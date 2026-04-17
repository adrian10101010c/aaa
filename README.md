-- Notificaciones
CREATE TABLE Notificaciones (
    Id INT IDENTITY(1,1) PRIMARY KEY,
    UsuarioDestinoId INT NOT NULL,
    Mensaje VARCHAR(200),
    Leido BIT DEFAULT 0, 
    Fecha DATETIME DEFAULT GETDATE(),

    CONSTRAINT FK_Notificacion_Usuario FOREIGN KEY (UsuarioDestinoId) 
    REFERENCES Usuarios(Id) ON DELETE CASCADE
);
