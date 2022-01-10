# tchad_product
une plateforme de vente des produits made in Tchad


#Projet Tchad_product

CREATE TABLE `fournisseur`(  
			    `id_four` INT(10) UNSIGNED AUTO_INCREMENT NOT NULL,
			    `nom_prenom` VARCHAR(100) NOT NULL,
			    `adresse` VARCHAR(200)  NULL,
			    `num_four`INT(10) NOT NULL,
			    PRIMARY KEY (`id_four`)
				);ENGINE=InnoDB;


insert into fournisseur (id_four, nom_prenom, adresse, num_four) values (1, 'Horton O''Dunneen', '486 Kenwood Way', '8053168');
insert into fournisseur (id_four, nom_prenom, adresse, num_four) values (2, 'Kacey Pilipyak', '92 Claremont Alley', '4215645');
insert into fournisseur (id_four, nom_prenom, adresse, num_four) values (3, 'Hobey Behr', '74 Ronald Regan Point', '1746237');
insert into fournisseur (id_four, nom_prenom, adresse, num_four) values (4, 'Thibaut Berlin', '74 Shelley Lane', '3514726');
insert into fournisseur (id_four, nom_prenom, adresse, num_four) values (5, 'Artemis Mingotti', '95 Pepper Wood Avenue', '7092972');
insert into fournisseur (id_four, nom_prenom, adresse, num_four) values (6, 'Corrie Kaplin', '8 Truax Drive', '6295637');
insert into fournisseur (id_four, nom_prenom, adresse, num_four) values (7, 'Abran Rubinsaft', '01 Scofield Street', '3555409');
insert into fournisseur (id_four, nom_prenom, adresse, num_four) values (8, 'Eziechiele Royl', '62280 Fisk Lane', '9567429');
insert into fournisseur (id_four, nom_prenom, adresse, num_four) values (9, 'Jozef Headan', '07 Pawling Court', '3712959');
insert into fournisseur (id_four, nom_prenom, adresse, num_four) values (10, 'Emera Charnley', '61537 Chinook Center', '5515176');

CREATE TABLE `tchad_product`.`produit` (
  `id_prod` INT(10) NOT NULL AUTO_INCREMENT,
  `nom` VARCHAR(100) NOT NULL,
  `description` VARCHAR(200) NOT NULL,
  `prixl` INT(100) NOT NULL,
  `id_four` INT(10) NOT NULL,
  PRIMARY KEY (`id_prod`),
  foreign key(`id_four`) references fournisseur(`id_four`),
) engine=InnoDB;
 


insert into produit (id_prod, nom, description, prix, id_four) values (1, 'Nitrogen', '', 77, 1);
insert into produit (id_prod, nom, description, prix, id_four) values (2, 'Onopordon Aurum', '', 71, 2);
insert into produit (id_prod, nom, description, prix, id_four) values (3, 'KETOROLAC TROMETHAMINE', '', 92, 3);
insert into produit (id_prod, nom, description, prix, id_four) values (4, 'amoxicillin', '', 36, 4);
insert into produit (id_prod, nom, description, prix, id_four) values (5, 'ethyl alcohol', '', 2, 5);
insert into produit (id_prod, nom, description, prix, id_four) values (6, 'Benzocaine', '', 89, 6);
insert into produit (id_prod, nom, description, prix, id_four) values (7, 'hydroxyzine pamoate', '', 81, 7);
insert into produit (id_prod, nom, description, prix, id_four) values (8, 'tretinoin', '', 87, 8);
insert into produit (id_prod, nom, description, prix, id_four) values (9, 'warfarin sodium', '', 25, 9);
insert into produit (id_prod, nom, description, prix, id_four) values (10, 'INTERLEUKIN-5', '', 90, 10);


CREATE TABLE `tchad_product`.`client` (
  `id_client` INT(10) NOT NULL AUTO_INCREMENT,
  `nom_prenom` VARCHAR(100) NOT NULL,
  `adresse` VARCHAR(200) NOT NULL,
  `num_client` INT(10) NOT NULL,
  `id_prod` INT(10) NOT NULL,
  PRIMARY KEY (`id_client`),
  foreign key(`id_prod`) references produit(`id_prod`),
) engine=InnoDB;
  


 insert into client (id_client, nom_prenom, adresse, num_client, id_prod) values (1, 'Rennie Waples', '885 Logan Parkway', '8107605', 1);
insert into client (id_client, nom_prenom, adresse, num_client, id_prod) values (2, 'Merrielle Alfonsetti', '65 Moose Terrace', '8849361', 2);
insert into client (id_client, nom_prenom, adresse, num_client, id_prod) values (3, 'Lucho Larimer', '079 Raven Avenue', '8264485', 3);
insert into client (id_client, nom_prenom, adresse, num_client, id_prod) values (4, 'Wildon Toffolini', '75 Sloan Point', '2193337', 4);
insert into client (id_client, nom_prenom, adresse, num_client, id_prod) values (5, 'Harlene Turpie', '6392 Fair Oaks Drive', '4783189', 5);
insert into client (id_client, nom_prenom, adresse, num_client, id_prod) values (6, 'Orlando Manass', '624 Norway Maple Court', '4014476', 6);
insert into client (id_client, nom_prenom, adresse, num_client, id_prod) values (7, 'Christalle Dudley', '1 Service Street', '2069862', 7);
insert into client (id_client, nom_prenom, adresse, num_client, id_prod) values (8, 'Sianna Dyzart', '8465 Warrior Lane', '7237812', 8);
insert into client (id_client, nom_prenom, adresse, num_client, id_prod) values (9, 'Spencer Screeton', '94 Lighthouse Bay Center', '8701471', 9);
insert into client (id_client, nom_prenom, adresse, num_client, id_prod) values (10, 'Lenette Blais', '7482 Shoshone Road', '5463321', 10
