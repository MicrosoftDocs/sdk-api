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

# _CERT_TEMPLATE_EXT structure


## -description


The <b>CERT_TEMPLATE_EXT</b> structure is a certificate template.


## -struct-fields




### -field pszObjId

<b>LPSTR</b> object identifier (OID).


### -field dwMajorVersion

<b>DWORD</b> indicating the major version of the template.


### -field fMinorVersion

<b>BOOL</b> flag set to <b>TRUE</b> if there is a minor version number.


### -field dwMinorVersion

<b>DWORD</b> indicating the minor version of the template.

