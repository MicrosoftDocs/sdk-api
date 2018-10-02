---
UID: NF:setupapi.SetupGetBinaryField
title: SetupGetBinaryField function
author: windows-sdk-content
description: The SetupGetBinaryField function retrieves binary data from a line in an INF file section, from the specified field to the end of the line.
old-location: setup\setupgetbinaryfield.htm
tech.root: SetupApi
ms.assetid: 6dfd4c8b-0197-4c6d-a780-084b428805b2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetupGetBinaryField, SetupGetBinaryField function [Setup API], _setupapi_setupgetbinaryfield, setup.setupgetbinaryfield, setupapi/SetupGetBinaryField
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupGetBinaryField
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupGetBinaryField function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetBinaryField</b> function retrieves binary data from a line in an INF file section, from the specified field to the end of the line.


## -parameters




### -param Context [in]

INF context for the line.


### -param FieldIndex [in]

The 1-based index of the starting field within the specified line from which the binary data should be retrieved. The binary data is built from each field, starting at this point to the end of the line. Each field corresponds to 1 byte and is in hexadecimal notation. A <i>FieldIndex</i> of zero is not valid with this function.


### -param ReturnBuffer [in, out]

Optional pointer to a buffer that receives the binary data. You should ensure the destination buffer is the same size or larger than the source buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. See the Remarks section.



### -param ReturnBufferSize [in]

Size of the buffer pointed to by <i>ReturnBuffer</i>, in characters. This number includes the <b>null</b> terminator. 


### -param RequiredSize [in, out]

Optional pointer to a variable that receives the required size for the buffer pointed to <i>ReturnBuffer</i>, in characters. This number includes the <b>null</b> terminator. If the size needed is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and a call to <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER. 



## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INVALID_DATA if a field that 
<b>SetupGetBinaryField</b> retrieves is not a valid hexadecimal number in the range 0-FF.




## -remarks



If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


To better understand how this function works, consider the following line from an INF file.

<pre class="syntax" xml:space="preserve"><code>X=34,FF,00,13</code></pre>
If 
<b>SetupGetBinaryField</b> was called on the preceding line, the binary values 34, FF, 00, and 13 would be put into the buffer specified by <i>ReturnBuffer</i>.

For the Unicode version of this function, the buffer sizes <i>ReturnBufferSize</i> and <i>RequiredSize</i> are specified in number of characters. This number includes the <b>null</b> terminator. For the ANSI version of this function, the sizes are specified in number of bytes.

If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Thus, you can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/4c77052a-46ef-4154-82c0-5ec447861bcf">SetupGetIntField</a>



<a href="https://msdn.microsoft.com/d884037c-a8d0-47a8-8b3f-70408866be05">SetupGetMultiSzField</a>



<a href="https://msdn.microsoft.com/fc735827-37ae-4d77-a0d4-4d31f0225d69">SetupGetStringField</a>
 

 

