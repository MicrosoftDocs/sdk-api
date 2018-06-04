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

# INTERNET_PER_CONN_OPTION_LISTW structure


## -description


Contains the list of options for a particular Internet connection.


## -struct-fields




### -field dwSize

Size of the 
structure, in bytes.


### -field pszConnection

Pointer to a string that contains the name of the RAS connection or <b>NULL</b>, which indicates the default or LAN connection, to set or query options on. 


### -field dwOptionCount

Number of options to query or set. 


### -field dwOptionError

Options that failed, if an error occurs. 


### -field pOptions

Pointer to an array of 
<a href="https://msdn.microsoft.com/35cfc768-1f1d-4be9-8d56-c56c7440513e">INTERNET_PER_CONN_OPTION</a> structures containing the options to query or set. 


## -remarks



In Microsoft Internet Explorer 5, only the ANSI versions of 
<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a> and 
<a href="https://msdn.microsoft.com/578c7130-7426-4a2e-ae0f-ed8a84449b06">InternetSetOption</a> will work with the 
<b>INTERNET_PER_CONN_OPTION_LIST</b> structure. The Unicode versions will support using the 
<b>INTERNET_PER_CONN_OPTION_LIST</b> structure in later versions of Internet Explorer.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/35cfc768-1f1d-4be9-8d56-c56c7440513e">INTERNET_PER_CONN_OPTION</a>



<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a>



<a href="https://msdn.microsoft.com/578c7130-7426-4a2e-ae0f-ed8a84449b06">InternetSetOption</a>
 

 

