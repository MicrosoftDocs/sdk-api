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

# EnumSystemCodePagesW function


## -description


Enumerates the code pages that are either installed on or supported by an operating system.


## -parameters




### -param lpCodePageEnumProc [in]

Pointer to an application-defined callback function. The <b>EnumSystemCodePages</b> function enumerates code pages by making repeated calls to this callback function. For more information, see <a href="https://msdn.microsoft.com/8573d519-bc1d-404b-b84f-1d746f014545">EnumCodePagesProc</a>.


### -param dwFlags [in]

Flag specifying the code pages to enumerate. This parameter can have one of the following values, which are mutually exclusive.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CP_INSTALLED"></a><a id="cp_installed"></a><dl>
<dt><b>CP_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate only installed code pages.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_SUPPORTED"></a><a id="cp_supported"></a><dl>
<dt><b>CP_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all supported code pages.

</td>
</tr>
</table>
 


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_BADDB. The function could not access the data. This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function enumerates the code pages by passing code page identifiers, one at a time, to the specified application-defined callback function. This process continues until all installed or supported code page identifiers have been passed to the callback function, or the callback function returns <b>FALSE</b>.

When an application is using this function to determine an appropriate code page for saving data, it should use Unicode when possible. Other code pages are not as portable as Unicode between vendors or operating systems, due to different implementations of the associated standards.




## -see-also




<a href="https://msdn.microsoft.com/8573d519-bc1d-404b-b84f-1d746f014545">EnumCodePagesProc</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

