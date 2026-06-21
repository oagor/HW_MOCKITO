package org.example;

import org.junit.jupiter.api.Assertions;
import org.junit.jupiter.api.Test;

public class MoviePosterManagerTest {

    @Test
    public void shouldReturnEmptyArrayWhenNoMovies() {
        MoviePosterManager manager = new MoviePosterManager();

        String[] expected = {};

        Assertions.assertArrayEquals(expected, manager.findAll());
        Assertions.assertArrayEquals(expected, manager.findLast());
    }

    @Test
    public void shouldAddOneMovie() {
        MoviePosterManager manager = new MoviePosterManager();

        manager.addMovie("Бладшот");

        String[] expected = {"Бладшот"};

        Assertions.assertArrayEquals(expected, manager.findAll());
    }

    @Test
    public void shouldAddSeveralMoviesAndReturnAllInOrder() {
        MoviePosterManager manager = new MoviePosterManager();

        manager.addMovie("Бладшот");
        manager.addMovie("Вперёд");
        manager.addMovie("Отель «Белград»");

        String[] expected = {
                "Бладшот",
                "Вперёд",
                "Отель «Белград»"
        };

        Assertions.assertArrayEquals(expected, manager.findAll());
    }

    @Test
    public void shouldReturnLastFiveByDefault() {
        MoviePosterManager manager = new MoviePosterManager();

        manager.addMovie("Бладшот");
        manager.addMovie("Вперёд");
        manager.addMovie("Отель «Белград»");
        manager.addMovie("Джентльмены");
        manager.addMovie("Человек-невидимка");
        manager.addMovie("Тролли. Мировой тур");
        manager.addMovie("Номер один");

        String[] expected = {
                "Номер один",
                "Тролли. Мировой тур",
                "Человек-невидимка",
                "Джентльмены",
                "Отель «Белград»"
        };

        Assertions.assertArrayEquals(expected, manager.findLast());
    }

    @Test
    public void shouldReturnLastThreeWhenLimitIsThree() {
        MoviePosterManager manager = new MoviePosterManager(3);

        manager.addMovie("Бладшот");
        manager.addMovie("Вперёд");
        manager.addMovie("Отель «Белград»");
        manager.addMovie("Джентльмены");

        String[] expected = {
                "Джентльмены",
                "Отель «Белград»",
                "Вперёд"
        };

        Assertions.assertArrayEquals(expected, manager.findLast());
    }
}
