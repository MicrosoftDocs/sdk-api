---
UID: TP:menurc
ms.assetid: b31c1492-ece3-3752-be79-c315513f21a3
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Menus and Other Resources



Overview of the Menus and Other Resources technology.

To develop Menus and Other Resources, you need these headers:

 * [resourceindexer.h](..\resourceindexer\index.md)
 * [shellapi.h](..\shellapi\index.md)
 * [strsafe.h](..\strsafe\index.md)
 * [verrsrc.h](..\verrsrc\index.md)
 * [winver.h](..\winver\index.md)

For the programming guide, see [Menus and Other Resources](/windows/desktop/menurc).

## Functions

| Title   | Description   |
| ---- |:---- |
| [CreateResourceIndexer function](..\resourceindexer\nf-resourceindexer-createresourceindexer.md) | Creates a new resource indexer for the specified paths of the root of the project files and the extension DLL. |
| [DestroyIndexedResults function](..\resourceindexer\nf-resourceindexer-destroyindexedresults.md) | Frees the parameters that the IndexFilePath method returned. |
| [DestroyResourceIndexer function](..\resourceindexer\nf-resourceindexer-destroyresourceindexer.md) | Frees the computational resources associated with the specified resource indexer. |
| [DuplicateIcon function](..\shellapi\nf-shellapi-duplicateicon.md) | Creates a duplicate of a specified icon. |
| [ExtractAssociatedIconA function](..\shellapi\nf-shellapi-extractassociatedicona.md) | Retrieves a handle to an indexed icon found in a file or an icon found in an associated executable file. |
| [ExtractAssociatedIconW function](..\shellapi\nf-shellapi-extractassociatediconw.md) | Retrieves a handle to an indexed icon found in a file or an icon found in an associated executable file. |
| [ExtractIconA function](..\shellapi\nf-shellapi-extracticona.md) | Retrieves a handle to an icon from the specified executable file, DLL, or icon file. |
| [ExtractIconExA function](..\shellapi\nf-shellapi-extracticonexa.md) | Creates an array of handles to large or small icons extracted from the specified executable file, DLL, or icon file. |
| [ExtractIconExW function](..\shellapi\nf-shellapi-extracticonexw.md) | Creates an array of handles to large or small icons extracted from the specified executable file, DLL, or icon file. |
| [ExtractIconW function](..\shellapi\nf-shellapi-extracticonw.md) | Retrieves a handle to an icon from the specified executable file, DLL, or icon file. |
| [GetFileVersionInfoA function](..\winver\nf-winver-getfileversioninfoa.md) | Retrieves version information for the specified file. |
| [GetFileVersionInfoExA function](..\winver\nf-winver-getfileversioninfoexa.md) | Retrieves version information for the specified file. |
| [GetFileVersionInfoExW function](..\winver\nf-winver-getfileversioninfoexw.md) | Retrieves version information for the specified file. |
| [GetFileVersionInfoSizeA function](..\winver\nf-winver-getfileversioninfosizea.md) | Determines whether the operating system can retrieve version information for a specified file. If version information is available, GetFileVersionInfoSize returns the size, in bytes, of that information. |
| [GetFileVersionInfoSizeExA function](..\winver\nf-winver-getfileversioninfosizeexa.md) | Determines whether the operating system can retrieve version information for a specified file. If version information is available, GetFileVersionInfoSizeEx returns the size, in bytes, of that information. |
| [GetFileVersionInfoSizeExW function](..\winver\nf-winver-getfileversioninfosizeexw.md) | Determines whether the operating system can retrieve version information for a specified file. If version information is available, GetFileVersionInfoSizeEx returns the size, in bytes, of that information. |
| [GetFileVersionInfoSizeW function](..\winver\nf-winver-getfileversioninfosizew.md) | Determines whether the operating system can retrieve version information for a specified file. If version information is available, GetFileVersionInfoSize returns the size, in bytes, of that information. |
| [GetFileVersionInfoW function](..\winver\nf-winver-getfileversioninfow.md) | Retrieves version information for the specified file. |
| [IndexFilePath function](..\resourceindexer\nf-resourceindexer-indexfilepath.md) | Indexes a file path for file and folder naming conventions. |
| [StringCbCatA function](..\strsafe\nf-strsafe-stringcbcata.md) | Concatenates one string to another string. |
| [StringCbCatExA function](..\strsafe\nf-strsafe-stringcbcatexa.md) | Concatenates one string to another string. |
| [StringCbCatExW function](..\strsafe\nf-strsafe-stringcbcatexw.md) | Concatenates one string to another string. |
| [StringCbCatNA function](..\strsafe\nf-strsafe-stringcbcatna.md) | Concatenates the specified number of bytes from one string to another string. |
| [StringCbCatNExA function](..\strsafe\nf-strsafe-stringcbcatnexa.md) | Concatenates the specified number of bytes from one string to another string. |
| [StringCbCatNExW function](..\strsafe\nf-strsafe-stringcbcatnexw.md) | Concatenates the specified number of bytes from one string to another string. |
| [StringCbCatNW function](..\strsafe\nf-strsafe-stringcbcatnw.md) | Concatenates the specified number of bytes from one string to another string. |
| [StringCbCatW function](..\strsafe\nf-strsafe-stringcbcatw.md) | Concatenates one string to another string. |
| [StringCbCopyA function](..\strsafe\nf-strsafe-stringcbcopya.md) | Copies one string to another. |
| [StringCbCopyExA function](..\strsafe\nf-strsafe-stringcbcopyexa.md) | Copies one string to another. |
| [StringCbCopyExW function](..\strsafe\nf-strsafe-stringcbcopyexw.md) | Copies one string to another. |
| [StringCbCopyNA function](..\strsafe\nf-strsafe-stringcbcopyna.md) | Copies the specified number of bytes from one string to another. |
| [StringCbCopyNExA function](..\strsafe\nf-strsafe-stringcbcopynexa.md) | Copies the specified number of bytes from one string to another. |
| [StringCbCopyNExW function](..\strsafe\nf-strsafe-stringcbcopynexw.md) | Copies the specified number of bytes from one string to another. |
| [StringCbCopyNW function](..\strsafe\nf-strsafe-stringcbcopynw.md) | Copies the specified number of bytes from one string to another. |
| [StringCbCopyW function](..\strsafe\nf-strsafe-stringcbcopyw.md) | Copies one string to another. |
| [StringCbGetsA function](..\strsafe\nf-strsafe-stringcbgetsa.md) | Gets one line of text from stdin, up to and including the newline character ('\n'). |
| [StringCbGetsExA function](..\strsafe\nf-strsafe-stringcbgetsexa.md) | Gets one line of text from stdin, up to and including the newline character ('\n'). |
| [StringCbGetsExW function](..\strsafe\nf-strsafe-stringcbgetsexw.md) | Gets one line of text from stdin, up to and including the newline character ('\n'). |
| [StringCbGetsW function](..\strsafe\nf-strsafe-stringcbgetsw.md) | Gets one line of text from stdin, up to and including the newline character ('\n'). |
| [StringCbLengthA function](..\strsafe\nf-strsafe-stringcblengtha.md) | Determines whether a string exceeds the specified length, in bytes. |
| [StringCbLengthW function](..\strsafe\nf-strsafe-stringcblengthw.md) | Determines whether a string exceeds the specified length, in bytes. |
| [StringCbPrintfA function](..\strsafe\nf-strsafe-stringcbprintfa.md) | Writes formatted data to the specified string. |
| [StringCbPrintfExA function](..\strsafe\nf-strsafe-stringcbprintfexa.md) | Writes formatted data to the specified string. |
| [StringCbPrintfExW function](..\strsafe\nf-strsafe-stringcbprintfexw.md) | Writes formatted data to the specified string. |
| [StringCbPrintfW function](..\strsafe\nf-strsafe-stringcbprintfw.md) | Writes formatted data to the specified string. |
| [StringCbPrintf_lA function](..\strsafe\nf-strsafe-stringcbprintf_la.md) | Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCbPrintf_lExA function](..\strsafe\nf-strsafe-stringcbprintf_lexa.md) | Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCbPrintf_lExW function](..\strsafe\nf-strsafe-stringcbprintf_lexw.md) | Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCbPrintf_lW function](..\strsafe\nf-strsafe-stringcbprintf_lw.md) | Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCbVPrintfA function](..\strsafe\nf-strsafe-stringcbvprintfa.md) | Writes formatted data to the specified string using a pointer to a list of arguments. |
| [StringCbVPrintfExA function](..\strsafe\nf-strsafe-stringcbvprintfexa.md) | Writes formatted data to the specified string using a pointer to a list of arguments. |
| [StringCbVPrintfExW function](..\strsafe\nf-strsafe-stringcbvprintfexw.md) | Writes formatted data to the specified string using a pointer to a list of arguments. |
| [StringCbVPrintfW function](..\strsafe\nf-strsafe-stringcbvprintfw.md) | Writes formatted data to the specified string using a pointer to a list of arguments. |
| [StringCbVPrintf_lA function](..\strsafe\nf-strsafe-stringcbvprintf_la.md) | Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCbVPrintf_lExA function](..\strsafe\nf-strsafe-stringcbvprintf_lexa.md) | Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCbVPrintf_lExW function](..\strsafe\nf-strsafe-stringcbvprintf_lexw.md) | Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCbVPrintf_lW function](..\strsafe\nf-strsafe-stringcbvprintf_lw.md) | Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCchCatA function](..\strsafe\nf-strsafe-stringcchcata.md) | Concatenates one string to another string. |
| [StringCchCatExA function](..\strsafe\nf-strsafe-stringcchcatexa.md) | Concatenates one string to another string. |
| [StringCchCatExW function](..\strsafe\nf-strsafe-stringcchcatexw.md) | Concatenates one string to another string. |
| [StringCchCatNA function](..\strsafe\nf-strsafe-stringcchcatna.md) | Concatenates the specified number of characters from one string to another string. |
| [StringCchCatNExA function](..\strsafe\nf-strsafe-stringcchcatnexa.md) | Concatenates the specified number of characters from one string to another string. |
| [StringCchCatNExW function](..\strsafe\nf-strsafe-stringcchcatnexw.md) | Concatenates the specified number of characters from one string to another string. |
| [StringCchCatNW function](..\strsafe\nf-strsafe-stringcchcatnw.md) | Concatenates the specified number of characters from one string to another string. |
| [StringCchCatW function](..\strsafe\nf-strsafe-stringcchcatw.md) | Concatenates one string to another string. |
| [StringCchCopyA function](..\strsafe\nf-strsafe-stringcchcopya.md) | Copies one string to another. |
| [StringCchCopyExA function](..\strsafe\nf-strsafe-stringcchcopyexa.md) | Copies one string to another. |
| [StringCchCopyExW function](..\strsafe\nf-strsafe-stringcchcopyexw.md) | Copies one string to another. |
| [StringCchCopyNA function](..\strsafe\nf-strsafe-stringcchcopyna.md) | Copies the specified number of characters from one string to another. |
| [StringCchCopyNExA function](..\strsafe\nf-strsafe-stringcchcopynexa.md) | Copies the specified number of characters from one string to another. |
| [StringCchCopyNExW function](..\strsafe\nf-strsafe-stringcchcopynexw.md) | Copies the specified number of characters from one string to another. |
| [StringCchCopyNW function](..\strsafe\nf-strsafe-stringcchcopynw.md) | Copies the specified number of characters from one string to another. |
| [StringCchCopyW function](..\strsafe\nf-strsafe-stringcchcopyw.md) | Copies one string to another. |
| [StringCchGetsA function](..\strsafe\nf-strsafe-stringcchgetsa.md) | Gets one line of text from stdin, up to and including the newline character ('\n'). |
| [StringCchGetsExA function](..\strsafe\nf-strsafe-stringcchgetsexa.md) | Gets one line of text from stdin, up to and including the newline character ('\n'). |
| [StringCchGetsExW function](..\strsafe\nf-strsafe-stringcchgetsexw.md) | Gets one line of text from stdin, up to and including the newline character ('\n'). |
| [StringCchGetsW function](..\strsafe\nf-strsafe-stringcchgetsw.md) | Gets one line of text from stdin, up to and including the newline character ('\n'). |
| [StringCchLengthA function](..\strsafe\nf-strsafe-stringcchlengtha.md) | Determines whether a string exceeds the specified length, in characters. |
| [StringCchLengthW function](..\strsafe\nf-strsafe-stringcchlengthw.md) | Determines whether a string exceeds the specified length, in characters. |
| [StringCchPrintfA function](..\strsafe\nf-strsafe-stringcchprintfa.md) | Writes formatted data to the specified string. |
| [StringCchPrintfExA function](..\strsafe\nf-strsafe-stringcchprintfexa.md) | Writes formatted data to the specified string. |
| [StringCchPrintfExW function](..\strsafe\nf-strsafe-stringcchprintfexw.md) | Writes formatted data to the specified string. |
| [StringCchPrintfW function](..\strsafe\nf-strsafe-stringcchprintfw.md) | Writes formatted data to the specified string. |
| [StringCchPrintf_lA function](..\strsafe\nf-strsafe-stringcchprintf_la.md) | Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCchPrintf_lExA function](..\strsafe\nf-strsafe-stringcchprintf_lexa.md) | Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCchPrintf_lExW function](..\strsafe\nf-strsafe-stringcchprintf_lexw.md) | Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCchPrintf_lW function](..\strsafe\nf-strsafe-stringcchprintf_lw.md) | Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCchVPrintfA function](..\strsafe\nf-strsafe-stringcchvprintfa.md) | Writes formatted data to the specified string using a pointer to a list of arguments. |
| [StringCchVPrintfExA function](..\strsafe\nf-strsafe-stringcchvprintfexa.md) | Writes formatted data to the specified string using a pointer to a list of arguments. |
| [StringCchVPrintfExW function](..\strsafe\nf-strsafe-stringcchvprintfexw.md) | Writes formatted data to the specified string using a pointer to a list of arguments. |
| [StringCchVPrintfW function](..\strsafe\nf-strsafe-stringcchvprintfw.md) | Writes formatted data to the specified string using a pointer to a list of arguments. |
| [StringCchVPrintf_lA function](..\strsafe\nf-strsafe-stringcchvprintf_la.md) | Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCchVPrintf_lExA function](..\strsafe\nf-strsafe-stringcchvprintf_lexa.md) | Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCchVPrintf_lExW function](..\strsafe\nf-strsafe-stringcchvprintf_lexw.md) | Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [StringCchVPrintf_lW function](..\strsafe\nf-strsafe-stringcchvprintf_lw.md) | Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. |
| [VerFindFileA function](..\winver\nf-winver-verfindfilea.md) | Determines where to install a file based on whether it locates another version of the file in the system. The values VerFindFile returns in the specified buffers are used in a subsequent call to the VerInstallFile function. |
| [VerFindFileW function](..\winver\nf-winver-verfindfilew.md) | Determines where to install a file based on whether it locates another version of the file in the system. The values VerFindFile returns in the specified buffers are used in a subsequent call to the VerInstallFile function. |
| [VerInstallFileA function](..\winver\nf-winver-verinstallfilea.md) | Installs the specified file based on information returned from the VerFindFile function. VerInstallFile decompresses the file, if necessary, assigns a unique filename, and checks for errors, such as outdated files. |
| [VerInstallFileW function](..\winver\nf-winver-verinstallfilew.md) | Installs the specified file based on information returned from the VerFindFile function. VerInstallFile decompresses the file, if necessary, assigns a unique filename, and checks for errors, such as outdated files. |
| [VerLanguageNameA function](..\winver\nf-winver-verlanguagenamea.md) | Retrieves a description string for the language associated with a specified binary Microsoft language identifier. |
| [VerLanguageNameW function](..\winver\nf-winver-verlanguagenamew.md) | Retrieves a description string for the language associated with a specified binary Microsoft language identifier. |
| [VerQueryValueA function](..\winver\nf-winver-verqueryvaluea.md) | Retrieves specified version information from the specified version-information resource. |
| [VerQueryValueW function](..\winver\nf-winver-verqueryvaluew.md) | Retrieves specified version information from the specified version-information resource. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [IndexedResourceQualifier structure](..\resourceindexer\ns-resourceindexer-indexedresourcequalifier.md) | Represents the context under which a resource is appropriate. |
| [tagVS_FIXEDFILEINFO structure](..\verrsrc\ns-verrsrc-tagvs_fixedfileinfo.md) | Contains version information for a file. This information is language and code page independent. |
