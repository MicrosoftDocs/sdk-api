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

# __MIDL___MIDL_itf_ads_0000_0000_0015 structure


## -description


The <b>ADS_DN_WITH_BINARY</b> structure is used with the <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structure to contain a distinguished name attribute value that also contains binary data.


## -struct-fields




### -field dwLength

Contains the length, in bytes, of the binary data in <b>lpBinaryValue</b>.


### -field lpBinaryValue

Pointer to an array of bytes that contains the binary data for the attribute. The <b>dwLength</b> member contains the number of bytes in this array.


### -field pszDNString

Pointer to a null-terminated Unicode string that contains the distinguished name.


## -remarks



When extending the active directory schema to add <b>ADS_DN_WITH_BINARY</b>, you must also specify the otherWellKnownGuid attribute definition. Add the following to the ldf file attribute definition: omObjectClass:: KoZIhvcUAQEBCw==




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a>



<a href="ad.win2k_s_object_dn_binary">Object(DN-Binary)</a>
 

 

