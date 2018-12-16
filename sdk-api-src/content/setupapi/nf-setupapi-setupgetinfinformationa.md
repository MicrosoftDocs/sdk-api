---
UID: NF:setupapi.SetupGetInfInformationA
title: SetupGetInfInformationA function
author: windows-sdk-content
description: The SetUpGetInfInformation function returns the SP_INF_INFORMATION structure for the specified INF file to a buffer.
old-location: setup\setupgetinfinformation.htm
tech.root: SetupApi
ms.assetid: 367eb374-1295-41f6-a1b3-cfc04e94b816
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupGetInfInformation, SetupGetInfInformation function [Setup API], SetupGetInfInformationA, SetupGetInfInformationW, _setupapi_setupgetinfinformation, setup.setupgetinfinformation, setupapi/SetupGetInfInformation, setupapi/SetupGetInfInformationA, setupapi/SetupGetInfInformationW
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupGetInfInformationW (Unicode) and SetupGetInfInformationA (ANSI)
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
 - SetupGetInfInformation
 - SetupGetInfInformationA
 - SetupGetInfInformationW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupGetInfInformationA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>SetUpGetInfInformation</b> function returns the 
<a href="https://msdn.microsoft.com/1fb08456-bc84-41a1-9f02-8fb499801831">SP_INF_INFORMATION</a> structure for the specified INF file to a buffer.


## -parameters




### -param InfSpec [in]

Handle or a file name for an INF file, depending on the value of <i>SearchControl</i>.


### -param SearchControl [in]

This parameter can be one of the following constants. 







#### INFINFO_INF_SPEC_IS_HINF

<i>InfSpec</i> is an INF handle. A single INF handle may reference multiple INF files if they have been append-loaded together. If it does, the structure returned by this function contains multiple sets of information.



#### INFINFO_INF_NAME_IS_ABSOLUTE

The string specified for <i>InfSpec</i> is a full path. No further processing is performed on <i>InfSpec</i>.



#### INFINFO_DEFAULT_SEARCH

Search the default locations for the INF file specified for <i>InfSpec</i>, which is assumed to be a filename only. The default locations are <i>%windir%</i>\<i>inf</i>, followed by <i>%windir%</i>\<i>system32</i>.



#### INFINFO_REVERSE_DEFAULT_SEARCH

Same as INFINFO_DEFAULT_SEARCH, except the default locations are searched in reverse order.



#### INFINFO_INF_PATH_LIST_SEARCH

Search for the INF in each of the directories listed in the <i>DevicePath</i> value entry under the following:<b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion</b>


### -param ReturnBuffer [in, out]

If not <b>NULL</b>, points to a buffer in which this function returns the <a href="https://msdn.microsoft.com/1fb08456-bc84-41a1-9f02-8fb499801831">SP_INF_INFORMATION</a> structure. 

You can call the function one time to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. For more information, see the Remarks section of this topic.


### -param ReturnBufferSize [in]

Size of  <i>ReturnBuffer</i>, in bytes.


### -param RequiredSize [in, out]

If not <b>NULL</b>, points to a variable in which this function returns the required size, in bytes, for the buffer pointed to by <i>ReturnBuffer</i>. 

If <i>ReturnBuffer</i> is specified and the size needed is larger than <i>ReturnBufferSize</i>, the function fails and a call to <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.



## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the INF file cannot be located, the function returns <b>FALSE</b> and a subsequent call to 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_FILE_NOT_FOUND.




## -remarks



If this function is called with a ReturnBuffer of <b>NULL</b> and a ReturnBufferSize of 0 (zero), the function puts the buffer size needed to hold the specified data into the variable pointed to by RequiredSize. If the function succeeds, the return value is a nonzero value. Otherwise, the return value is 0 (zero), and extended error information can be obtained by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/36f1824d-f71e-462a-a233-0240e76de3d2">SetupQueryInfFileInformation</a>



<a href="https://msdn.microsoft.com/58768b91-a0c7-4791-8667-2890b742798c">SetupQueryInfVersionInformation</a>
 

 

