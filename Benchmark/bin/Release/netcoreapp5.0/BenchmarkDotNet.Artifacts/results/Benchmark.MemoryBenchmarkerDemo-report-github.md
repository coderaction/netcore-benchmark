``` ini

BenchmarkDotNet=v0.12.1, OS=macOS 11.1 (20C69) [Darwin 20.2.0]
Intel Core i9-8950HK CPU 2.90GHz (Coffee Lake), 1 CPU, 12 logical and 6 physical cores
.NET Core SDK=5.0.101
  [Host]     : .NET Core 5.0.1 (CoreCLR 5.0.120.57516, CoreFX 5.0.120.57516), X64 RyuJIT
  DefaultJob : .NET Core 5.0.1 (CoreCLR 5.0.120.57516, CoreFX 5.0.120.57516), X64 RyuJIT


```
|                          Method |      Mean |     Error |    StdDev |     Gen 0 |     Gen 1 |    Gen 2 | Allocated |
|-------------------------------- |----------:|----------:|----------:|----------:|----------:|---------:|----------:|
| ConcatStringsUsingStringBuilder |  6.111 ms | 0.1183 ms | 0.1049 ms | 2867.1875 | 1867.1875 | 968.7500 |  14.86 MB |
|   ConcatStringsUsingGenericList | 19.395 ms | 0.3853 ms | 0.5011 ms | 1531.2500 |  687.5000 | 281.2500 |   9.16 MB |
