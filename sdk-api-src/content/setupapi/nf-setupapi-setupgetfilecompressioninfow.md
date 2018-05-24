---
UID: NF:setupapi.SetupGetFileCompressionInfoW
title: SetupGetFileCompressionInfoW function
author: windows-driver-content
description: The SetupGetFileCompressionInfo function examines a physical file to determine if it is compressed and gets its full path, size, and the size of the uncompressed target file.
old-location: setup\setupgetfilecompressioninfo.htm
old-project: SetupApi
ms.assetid: 68bcfbb3-f0ba-412b-9ed2-e2139099fcf2
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SetupGetFileCompressionInfo, SetupGetFileCompressionInfo function [Setup API], SetupGetFileCompressionInfoA, SetupGetFileCompressionInfoW, _setupapi_setupgetfilecompressioninfo, setup.setupgetfilecompressioninfo, setupapi/SetupGetFileCompressionInfo, setupapi/SetupGetFileCompressionInfoA, setupapi/SetupGetFileCompressionInfoW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupGetFileCompressionInfo
-	SetupGetFileCompressionInfoA
-	SetupGetFileCompressionInfoW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupGetFileCompressionInfoW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetFileCompressionInfo</b> function examines a physical file to determine if it is compressed and gets its full path, size, and the size of the uncompressed target file.

Note that this function is obsolete and has been replaced by 
<a href="https://msdn.microsoft.com/e6f01e02-ea39-4b25-bcc0-2aee941c7834">SetupGetFileCompressionInfoEx</a>. Do not use 
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



The function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> that indicates the outcome of the file search. The error code can be one of the following values.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Do not use 
<b>SetupGetFileCompressionInfo</b>, instead always use 
<a href="https://msdn.microsoft.com/e6f01e02-ea39-4b25-bcc0-2aee941c7834">SetupGetFileCompressionInfoEx</a>.

Because 
<b>SetupGetFileCompressionInfo</b> determines the compression by referencing the physical file, your setup application should ensure that the file is present before calling 
<b>SetupGetFileCompressionInfo</b>.

Note that if the version of SetupAPI.dll is less than 5.0.2195, then the caller needs to use the exported function <b>MyFree</b> from SetupAPI to free the memory allocated by this function, rather then using <b>LocalFree</b>. If the call to <b>LocalFree</b>  causes an Access Violation, you should solve the problem by using <b>MyFree</b>. 

The following is an example of how to obtain the <b>MyFree</b> function from the SetupAPI.dll: 


<pre class="syntax" xml:space="preserve"><code>typedef VOID (WINAPI* MYFREEFUNC)(LPVOID lpBuff);
   MYFREEFUNC MyFree;

   HMODULE hDll=NULL;
   hDll = GetModuleHandle("SETUPAPI.DLL");
   MyFree = (MYFREEFUNC)GetProcAddress(hDll, "MyFree");
   ...
   other code here to prepare file queue
   ...
   PTSTR lpActualSourceFileName;
   SetupGetFileCompressionInfo(...,&amp;lpActualSourceFileName,...,...,...);
   ...
   MyFree(lpActualSourceFileName); </code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/6058567b-fa34-472b-91d8-3c5f9ee741b1">SetupDecompressOrCopyFile</a>
 

 

