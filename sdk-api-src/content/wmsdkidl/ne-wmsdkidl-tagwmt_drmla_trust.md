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

# tagWMT_DRMLA_TRUST enumeration


## -description



Defines the trust state of a DRM license acquisition URL.




## -enum-fields




### -field WMT_DRMLA_UNTRUSTED

Indicates that the validity of the license acquisition URL cannot be guaranteed because it is not signed. All protected content created prior to Windows Media 9 Series will cause this value to be returned.


### -field WMT_DRMLA_TRUSTED

Indicates that the license acquisition URL is the original one provided with the content.


### -field WMT_DRMLA_TAMPERED

Indicates that the license acquisition URL was originally signed and has been tampered with.


## -remarks



When a <b>WMT_LICENSEURL_SIGNATURE_STATE</b> message is received in the <b>OnStatus</b> callback method, pValue will be set to one of the <b>WMT_DRMLA_TRUST</b> constants, which indicate whether there is any problem with the digital signature applied to the license acquisition URL.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

