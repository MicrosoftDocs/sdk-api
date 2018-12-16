---
UID: NF:setupapi.SetupGetStringFieldW
title: SetupGetStringFieldW function
author: windows-sdk-content
description: The SetupGetStringField function retrieves a string from the specified field of a line in an INF file.
old-location: setup\setupgetstringfield.htm
tech.root: SetupApi
ms.assetid: fc735827-37ae-4d77-a0d4-4d31f0225d69
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupGetStringField, SetupGetStringField function [Setup API], SetupGetStringFieldA, SetupGetStringFieldW, _setupapi_setupgetstringfield, setup.setupgetstringfield, setupapi/SetupGetStringField, setupapi/SetupGetStringFieldA, setupapi/SetupGetStringFieldW
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetStringFieldW (Unicode) and SetupGetStringFieldA (ANSI)
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
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
 - SetupGetStringField
 - SetupGetStringFieldA
 - SetupGetStringFieldW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupGetStringFieldW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetStringField</b> function retrieves a string from the specified field of a line in an INF file.


## -parameters




### -param Context [in]

Pointer to the context for a line in an INF file.


### -param FieldIndex [in]

The 1-based index of the field within the specified line from which the string should be retrieved. Use a <i>FieldIndex</i> of 0 to retrieve a string key, if present.


### -param ReturnBuffer [in, out]

Optional pointer to a  buffer that receives the <b>null</b>-terminated string. You should ensure the destination buffer is the same size or larger than the source buffer.  This parameter can be <b>NULL</b>. See the Remarks section. 


### -param ReturnBufferSize [in]

Size of the buffer pointed to by <i>ReturnBuffer</i>, in characters. This includes the <b>null</b> terminator. 


### -param RequiredSize [out]

Optional pointer to a variable that receives the required size  for the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. If <i>ReturnBuffer</i> is specified and the actual size needed is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and does not store the string in the buffer. In this case, a call to <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.  For the Unicode version of this function, the required size is in characters. This includes the <b>null</b> terminator. 



## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size.



Note that the maximum length of any single string specified in an INF Strings section is 512 characters, including the terminating <b>NULL</b>. If the string length is greater than 512 it will be truncated and no error will be returned. The maximum length of any concatenated string created from one or more %strkey% tokens is 4096 characters.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/6dfd4c8b-0197-4c6d-a780-084b428805b2">SetupGetBinaryField</a>



<a href="https://msdn.microsoft.com/4c77052a-46ef-4154-82c0-5ec447861bcf">SetupGetIntField</a>



<a href="https://msdn.microsoft.com/d884037c-a8d0-47a8-8b3f-70408866be05">SetupGetMultiSzField</a>
 

 

