---
UID: NF:winnls.IsDBCSLeadByteEx
title: IsDBCSLeadByteEx function
author: windows-sdk-content
description: Determines if a specified character is potentially a lead byte. A lead byte is the first byte of a two-byte character in a double-byte character set (DBCS) for the code page.
old-location: intl\isdbcsleadbyteex.htm
old-project: Intl
ms.assetid: 1ca67e7e-a2a7-433f-b2b6-8fa5ecc50354
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CP_ACP, CP_MACCP, CP_OEMCP, CP_THREAD_ACP, IsDBCSLeadByteEx, IsDBCSLeadByteEx function [Internationalization for Windows Applications], _win32_IsDBCSLeadByteEx, intl.isdbcsleadbyteex, winnls/IsDBCSLeadByteEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NORM_FORM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - IsDBCSLeadByteEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IsDBCSLeadByteEx function


## -description


Determines if a specified character is potentially a lead byte. A lead byte is the first byte of a two-byte character in a <a href="https://msdn.microsoft.com/df049d22-02e2-48b2-8b74-52f71c00c549">double-byte character set</a> (DBCS) for the code page.


## -parameters




### -param CodePage [in]

Identifier of the code page used to check lead byte ranges. This parameter can be one of the code page identifiers defined in <a href="https://msdn.microsoft.com/647c9e14-f134-4300-bf17-6f6321db6477">Unicode and Character Set Constants</a> or one of the following predefined values. This function validates lead byte values only in code pages 932, 936, 949, 950, and 1361.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CP_ACP"></a><a id="cp_acp"></a><dl>
<dt><b>CP_ACP</b></dt>
</dl>
</td>
<td width="60%">
Use system default Windows ANSI code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_MACCP"></a><a id="cp_maccp"></a><dl>
<dt><b>CP_MACCP</b></dt>
</dl>
</td>
<td width="60%">
Use the system default Macintosh code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_OEMCP"></a><a id="cp_oemcp"></a><dl>
<dt><b>CP_OEMCP</b></dt>
</dl>
</td>
<td width="60%">
Use system default OEM code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_THREAD_ACP"></a><a id="cp_thread_acp"></a><dl>
<dt><b>CP_THREAD_ACP</b></dt>
</dl>
</td>
<td width="60%">
Use the Windows ANSI code page for the current thread.

</td>
</tr>
</table>
 


### -param TestChar [in]

The character to test.


## -returns



Returns a nonzero value if the byte is a lead byte. The function returns 0 if the byte is not a lead byte or if the character is a single-byte character. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>   This function does not validate the presence or validity of a trail byte. Therefore, <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> might not recognize a sequence that the application using <a href="https://msdn.microsoft.com/13767af5-9313-4c11-8386-fe41c7720d49">IsDBCSLeadByte</a> reports as a lead byte. The application can easily become unsynchronized with the results of <b>MultiByteToWideChar</b>, potentially leading to unexpected errors or buffer size mismatches.</div>
<div> </div>
In general, instead of attempting low-level manipulation of code page data, applications should use <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> to convert the data to UTF-16 and work with it in that encoding.

Lead byte values are specific to each distinct DBCS. Some byte values can appear in a single code page as both the lead and trail byte of a DBCS character. Thus, <b>IsDBCSLeadByteEx</b> can only indicate a potential lead byte value.

To make sense of a DBCS string, an application normally starts at the beginning of the string and scans forward, keeping track when it encounters a lead byte, and treating the next byte as the trailing part of the same character. To back up, the application should use <a href="_win32_CharPrevExA_cpp">CharPrevExA</a> instead of attempting to develop its own algorithm.




## -see-also




<a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a>



<a href="https://msdn.microsoft.com/1799f5da-1391-4b6e-ac13-718017a77557">Unicode and Character Set Functions</a>



<a href="https://msdn.microsoft.com/8c1c6582-b58c-4008-9ce5-208acc191d9f">Unicode and Character Sets</a>



<a href="https://msdn.microsoft.com/b8c13444-86ab-479c-ac04-9b184d9eebf6">WideCharToMultiByte</a>
 

 

