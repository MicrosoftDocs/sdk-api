---
UID: NF:setupapi.SetupQueryInfVersionInformationA
title: SetupQueryInfVersionInformationA function
author: windows-sdk-content
description: The SetupQueryInfVersionInformation function returns INF file version information from an SP_INF_INFORMATION structure to a buffer.
old-location: setup\setupqueryinfversioninformation.htm
old-project: SetupApi
ms.assetid: 58768b91-a0c7-4791-8667-2890b742798c
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SetupQueryInfVersionInformation, SetupQueryInfVersionInformation function [Setup API], SetupQueryInfVersionInformationA, SetupQueryInfVersionInformationW, _setupapi_setupqueryinfversioninformation, setup.setupqueryinfversioninformation, setupapi/SetupQueryInfVersionInformation, setupapi/SetupQueryInfVersionInformationA, setupapi/SetupQueryInfVersionInformationW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueryInfVersionInformationW (Unicode) and SetupQueryInfVersionInformationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupQueryInfVersionInformation
 - SetupQueryInfVersionInformationA
 - SetupQueryInfVersionInformationW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupQueryInfVersionInformationA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueryInfVersionInformation</b> function returns INF file version information from an 
<a href="https://msdn.microsoft.com/1fb08456-bc84-41a1-9f02-8fb499801831">SP_INF_INFORMATION</a> structure to a buffer.


## -parameters




### -param InfInformation [in]

Pointer to an 
<a href="https://msdn.microsoft.com/1fb08456-bc84-41a1-9f02-8fb499801831">SP_INF_INFORMATION</a> structure previously returned from a call to the 
<a href="https://msdn.microsoft.com/367eb374-1295-41f6-a1b3-cfc04e94b816">SetupGetInfInformation</a> function.


### -param InfIndex [in]

Index of the constituent INF file to retrieve version information from. This index can be in the range [0, <i>InfInformation.InfCount</i>). Meaning that the values zero through, but not including, <i>InfInformation.InfCount</i> are valid.


### -param Key [in]

Optional pointer to a <b>null</b>-terminated string containing the key name whose associated string is to be retrieved. If this parameter is <b>NULL</b>, all resource keys are copied to the supplied buffer. Each string is <b>null</b>-terminated, with an extra <b>null</b> at the end of the list.


### -param ReturnBuffer [in, out]

If not <b>NULL</b>, <i>ReturnBuffer</i> points to a call-supplied character buffer in which this function returns the INF file style. You should use a <b>null</b>-terminated string. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. See the Remarks section. This parameter can be <b>NULL</b>.



### -param ReturnBufferSize [in]

Size of the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This number includes the <b>null</b> terminator. 



### -param RequiredSize [in, out]

If not <b>NULL</b>, pointer to a variable that receives the size required for the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This number includes the <b>null</b> terminator. If <i>ReturnBuffer</i> is specified and the actual size is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and a call to 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.  


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If 
<b>SetupQueryInfVersionInformation</b> is called on a legacy INF file , then version information is generated from the legacy INF file in the following manner:

<ol>
<li>The OptionType key in the <b>Identification</b> section of the legacy file  is returned as the Class key value.</li>
<li>The FileType key in the <b>Signature</b> section of the legacy INF file becomes the Signature key value.</li>
<li>If the value of the FileType key of the legacy INF file is MICROSOFT_FILE, then the Provider key value is set to "Microsoft".</li>
</ol>
The following table summarizes how the information is translated before it is passed into the 
<a href="https://msdn.microsoft.com/1fb08456-bc84-41a1-9f02-8fb499801831">SP_INF_INFORMATION</a> structure.

<table>
<tr>
<th>Legacy file information</th>
<th> Windows INF information</th>
</tr>
<tr>
<td>
<pre class="syntax" xml:space="preserve"><code>[Identification]
OptionType = Mouse</code></pre>
</td>
<td>
<pre class="syntax" xml:space="preserve"><code>[Version]
Class=Mouse</code></pre>
</td>
</tr>
<tr>
<td>
<pre class="syntax" xml:space="preserve"><code>[Signature]
FileType = MICROSOFT_FILE</code></pre>
</td>
<td>
<pre class="syntax" xml:space="preserve"><code>Signature=MICROSOFT_FILE</code></pre>
</td>
</tr>
<tr>
<td>(if the FileType is MICROSOFT_FILE)</td>
<td>
<pre class="syntax" xml:space="preserve"><code>Provider="Microsoft"</code></pre>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/367eb374-1295-41f6-a1b3-cfc04e94b816">SetupGetInfInformation</a>



<a href="https://msdn.microsoft.com/36f1824d-f71e-462a-a233-0240e76de3d2">SetupQueryInfFileInformation</a>
 

 

