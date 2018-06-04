---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SetupEnumInfSectionsA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>SetupEnumInfSections</b> function retrieves section names from an INF file.


## -parameters




### -param InfHandle [in]

Handle to the INF file that is to be queried.


### -param Index

TBD


### -param Buffer

TBD


### -param Size

TBD


### -param SizeNeeded

TBD




#### - EnumerationIndex [in]

The zero-based index of the section name to retrieve. This index may not correspond to the order of sections as they appear in the INF file.


#### - RequiredSize [out, optional]

Pointer to a location that receives the required size of the buffer pointed to by <i>ReturnBuffer</i>. The size is specified as the number of characters required to store the section name, including the terminating <b>NULL</b> character.


#### - ReturnBuffer [out, optional]

Pointer to a buffer that receives the section name. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the name. Using this technique, you can avoid errors caused by an insufficient buffer size. This parameter is optional. For more information, see the Remarks section.


#### - ReturnBufferSize [in]

Size of the buffer pointed to by <i>ReturnBuffer</i> in characters. This number includes the terminating <b>NULL</b> character.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_NO_MORE_ITEMS</b> if the value of <b>EnumerationIndex</b> is greater than or equal to the number of sections names in the INF file.




## -remarks



This function can enumerate all unique section names in the INF file. If a section name appears more than once in an INF file, the function returns the name only once using a single enumeration index. To return all section names in the INF file, call the function beginning with an enumeration index of zero and then make repeated calls to the function while incrementing the index until the function returns  <b>FALSE</b> and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_NO_MORE_ITEMS</b>.  Your application should not rely on the section names being returned in any order based on the enumeration index.



