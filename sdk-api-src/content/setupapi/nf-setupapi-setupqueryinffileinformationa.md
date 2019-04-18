---
UID: NF:setupapi.SetupQueryInfFileInformationA
title: SetupQueryInfFileInformationA function (setupapi.h)
author: windows-sdk-content
description: The SetupQueryInfFileInformation function returns an INF filename from an SP_INF_INFORMATION structure to a buffer.
old-location: setup\setupqueryinffileinformation.htm
tech.root: SetupApi
ms.assetid: 36f1824d-f71e-462a-a233-0240e76de3d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupQueryInfFileInformation, SetupQueryInfFileInformation function [Setup API], SetupQueryInfFileInformationA, SetupQueryInfFileInformationW, _setupapi_setupqueryinffileinformation, setup.setupqueryinffileinformation, setupapi/SetupQueryInfFileInformation, setupapi/SetupQueryInfFileInformationA, setupapi/SetupQueryInfFileInformationW
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueryInfFileInformationW (Unicode) and SetupQueryInfFileInformationA (ANSI)
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
 - SetupQueryInfFileInformation
 - SetupQueryInfFileInformationA
 - SetupQueryInfFileInformationW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupQueryInfFileInformationA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueryInfFileInformation</b> function returns an INF filename from an 
<a href="https://msdn.microsoft.com/1fb08456-bc84-41a1-9f02-8fb499801831">SP_INF_INFORMATION</a> structure to a buffer.


## -parameters




### -param InfInformation [in]

Pointer to an 
<a href="https://msdn.microsoft.com/1fb08456-bc84-41a1-9f02-8fb499801831">SP_INF_INFORMATION</a> structure returned from a call to the 
<a href="https://msdn.microsoft.com/367eb374-1295-41f6-a1b3-cfc04e94b816">SetupGetInfInformation</a> function.


### -param InfIndex [in]

Index of the constituent INF filename to retrieve. This index can be in the range [0, <i>InfInformation.InfCount</i>). Meaning that the values zero through, but not including, <i>InfInformation.InfCount</i> are valid.


### -param ReturnBuffer [in, out]

If not <b>NULL</b>, <i>ReturnBuffer</i> is a pointer to a buffer in which this function returns the full INF filename. You should use a <b>null</b>-terminated string. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. See the Remarks section. Using this technique, you can avoid errors due to an insufficient buffer size. This parameter can be <b>NULL</b>.


### -param ReturnBufferSize [in]

Size of the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This includes the <b>null</b> terminator. 


### -param RequiredSize [in, out]

If not <b>NULL</b>, pointer to a variable that receives the required size for the <i>ReturnBuffer</i> buffer, in characters. This includes the <b>null</b> terminator. If <i>ReturnBuffer</i> is specified and the actual size is larger than <i>ReturnBufferSize</i>, the function fails and a call to <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER. 



## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.





## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/367eb374-1295-41f6-a1b3-cfc04e94b816">SetupGetInfInformation</a>



<a href="https://msdn.microsoft.com/58768b91-a0c7-4791-8667-2890b742798c">SetupQueryInfVersionInformation</a>
 

 

