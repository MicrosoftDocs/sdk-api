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

# AM_DVDCOPYSTATE enumeration


## -description



Specifies the copy protection state.




## -enum-fields




### -field AM_DVDCOPYSTATE_INITIALIZE

Starting a full key-exchange algorithm.


### -field AM_DVDCOPYSTATE_INITIALIZE_TITLE

Starting a title key-exchange algorithm.


### -field AM_DVDCOPYSTATE_AUTHENTICATION_NOT_REQUIRED

Authentication is not required.  


### -field AM_DVDCOPYSTATE_AUTHENTICATION_REQUIRED

Authentication required.


### -field AM_DVDCOPYSTATE_DONE

Key exchange negotiation is complete.


## -remarks



The <a href="https://msdn.microsoft.com/0ad15402-096c-4967-bebc-10652535e502">AM_DVDCOPY_SET_COPY_STATE</a> structure uses this data type.




## -see-also




<a href="https://msdn.microsoft.com/da3abefd-8f25-449d-8787-84d2cef928da">DVD Copy Protection Property Set</a>
 

 

