## Install Maven

Menginstal Maven sebagai build tool untuk proyek Java.

```bash
sudo apt install maven
```

## Mengunduh Dependency

Mengunduh dan menginstal seluruh dependency yang didefinisikan pada file `pom.xml`.

```bash
mvn clean install
```

## Menambahkan Plugin OWASP Dependency Check

Menambahkan plugin OWASP Dependency Check pada `pom.xml` untuk melakukan audit keamanan dependency.

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.owasp</groupId>
            <artifactId>dependency-check-maven</artifactId>
            <version>12.1.0</version>
        </plugin>
    </plugins>
</build>
```

## Menjalankan Audit Dependency

Memindai seluruh dependency dan mendeteksi kerentanan keamanan berdasarkan database CVE.

```bash
mvn dependency-check:check
```

## Membuka Laporan Hasil

Laporan hasil pemindaian tersedia pada lokasi berikut:

```text
target/dependency-check-report.html
```
