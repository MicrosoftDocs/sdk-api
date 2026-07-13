---
UID: NF:setupapi.SetupGetFileCompressionInfoW
title: SetupGetFileCompressionInfoW function (setupapi.h)
description: The SetupGetFileCompressionInfo function examines a physical file to determine if it is compressed and gets its full path, size, and the size of the uncompressed target file. (Unicode)
helpviewer_keywords: ["SetupGetFileCompressionInfo", "SetupGetFileCompressionInfo function [Setup API]", "SetupGetFileCompressionInfoW", "_setupapi_setupgetfilecompressioninfo", "setup.setupgetfilecompressioninfo", "setupapi/SetupGetFileCompressionInfo", "setupapi/SetupGetFileCompressionInfoW"]
old-location: setup\setupgetfilecompressioninfo.htm
tech.root: setup
ms.assetid: 68bcfbb3-f0ba-412b-9ed2-e2139099fcf2
ms.date: 12/05/2018
ms.keywords: SetupGetFileCompressionInfo, SetupGetFileCompressionInfo function [Setup API], SetupGetFileCompressionInfoA, SetupGetFileCompressionInfoW, _setupapi_setupgetfilecompressioninfo, setup.setupgetfilecompressioninfo, setupapi/SetupGetFileCompressionInfo, setupapi/SetupGetFileCompressionInfoA, setupapi/SetupGetFileCompressionInfoW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetFileCompressionInfoW (Unicode) and SetupGetFileCompressionInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupGetFileCompressionInfoW
 - setupapi/SetupGetFileCompressionInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupGetFileCompressionInfo
 - SetupGetFileCompressionInfoA
 - SetupGetFileCompressionInfoW
---

# SetupGetFileCompressionInfoW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetFileCompressionInfo</b> function examines a physical file to determine if it is compressed and gets its full path, size, and the size of the uncompressed target file.

Note that this function is obsolete and has been replaced by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetfilecompressioninfoexa">SetupGetFileCompressionInfoEx</a>. Do not use 
<b>SetupGetFileCompressionInfo</b>, instead always use 
<b>SetupGetFileCompressionInfoEx</b>.

## -parameters

### -param SourceFileName [in]

File name of the file about which information is required. If the file is not found on the source media exactly as named, the file is searched for with up to two alternate "compressed-form" names. For example, if the file is F:\x86\cmd.exe and it is not found, F:\mpis\cmd.ex_ is searched for and, if that is not found, a search is done for F:\x86\cmd.ex$. You should use a null-terminated string.

### -param ActualSourceFileName [in, out]

Pointer to a variable that receives the full path of the file that it has been able to locate. The caller can free the pointer with a call to <b>LocalFree</b>. The path is valid only if the function returns NO_ERROR. Note that if the version of SetupAPI.dll is less than 5.0.2195, then the caller needs to use the exported function <b>MyFree</b> from SetupAPI to free the memory allocated by this function, rather then using <b>LocalFree</b>. See the Remarks section.

### -param SourceFileSize [in, out]

Pointer to a variable in which this function returns the size of the file in its current form which is the current size of the file named by <i>ActualSourceFileName</i>. The size is determined by examining the source file; it is not retrieved from an INF file. The source file size is valid only if the function returns NO_ERROR.

### -param TargetFileSize [in, out]

Pointer to a variable in which this function returns the size the file will occupy when it is uncompressed or copied. If the file is not compressed, this value will be the same as <i>SourceFileSize</i>. The size is determined by examining the file; it is not retrieved from an INF file. The target file size is valid only if the function returns NO_ERROR.

### -param CompressionType [in, out]

Pointer to a variable in which this function returns a value indicating the type of compression used on <i>ActualSourceFileName</i>. The compression type is valid only if the function returns NO_ERROR. The value can be one of the following flags. 







#### FILE_COMPRESSION_NONE

The source file is not compressed with a recognized compression algorithm.



#### FILE_COMPRESSION_WINLZA

The source file is compressed with LZ compression.



#### FILE_COMPRESSION_MSZIP

The source file is compressed with MSZIP compression.


##### - CompressionType.FILE_COMPRESSION_MSZIP

The source file is compressed with MSZIP compression.


##### - CompressionType.FILE_COMPRESSION_NONE

The source file is not compressed with a recognized compression algorithm.


##### - CompressionType.FILE_COMPRESSION_WINLZA

The source file is compressed with LZ compression.

## -returns

The function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> that indicates the outcome of the file search. The error code can be one of the following values.

To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Do not use 
<b>SetupGetFileCompressionInfo</b>, instead always use 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetfilecompressioninfoexa">SetupGetFileCompressionInfoEx</a>.

Because 
<b>SetupGetFileCompressionInfo</b> determines the compression by referencing the physical file, your setup application should ensure that the file is present before calling 
<b>SetupGetFileCompressionInfo</b>.

Note that if the version of SetupAPI.dll is less than 5.0.2195, then the caller needs to use the exported function <b>MyFree</b> from SetupAPI to free the memory allocated by this function, rather then using <b>LocalFree</b>. If the call to <b>LocalFree</b>  causes an Access Violation, you should solve the problem by using <b>MyFree</b>. 

The following is an example of how to obtain the <b>MyFree</b> function from the SetupAPI.dll: 



``` syntax
typedef VOID (WINAPI* MYFREEFUNC)(LPVOID lpBuff);
   MYFREEFUNC MyFree;

   HMODULE hDll=NULL;
   hDll = GetModuleHandle("SETUPAPI.DLL");
   MyFree = (MYFREEFUNC)GetProcAddress(hDll, "MyFree");
   ...
   other code here to prepare file queue
   ...
   PTSTR lpActualSourceFileName;
   SetupGetFileCompressionInfo(...,&lpActualSourceFileName,...,...,...);
   ...
   MyFree(lpActualSourceFileName); 
```





> [!NOTE]
> The setupapi.h header defines SetupGetFileCompressionInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdecompressorcopyfilea">SetupDecompressOrCopyFile</a>
