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

# _CMC_ADD_EXTENSIONS_INFO structure


## -description


The <b>CMC_ADD_EXTENSIONS_INFO</b> structure contains certificate extension control attributes to be added to a certificate.


## -struct-fields




### -field dwCmcDataReference

<b>DWORD</b> data reference number.


### -field cCertReference

<b>DWORD</b> count of elements in the <b>rgdwCertReference</b> array.


### -field rgdwCertReference

Array of certificate reference numbers.


### -field cExtension

<b>DWORD</b> count of the elements in the <b>rgExtension</b> array.


### -field rgExtension

Array of pointers to the 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> certificate extensions to be added.

