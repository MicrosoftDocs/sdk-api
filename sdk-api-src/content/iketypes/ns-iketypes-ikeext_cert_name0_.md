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

# IKEEXT_CERT_NAME0_ structure


## -description


The <b>IKEEXT_CERT_NAME0</b> structure specifies certificate selection "subject" criteria for an authentication method.


## -struct-fields




### -field nameType

Type: <b><a href="https://msdn.microsoft.com/ec59d6b2-3bfc-4e5b-9222-609d3141db5c">IKEEXT_CERT_CRITERIA_NAME_TYPE</a></b>

The type of NAME field.


### -field certName

Type: <b>LPWSTR</b>

The string to be used for matching the "subject" criteria.


## -see-also




<a href="https://msdn.microsoft.com/ec59d6b2-3bfc-4e5b-9222-609d3141db5c">IKEEXT_CERT_CRITERIA_NAME_TYPE</a>
 

 

