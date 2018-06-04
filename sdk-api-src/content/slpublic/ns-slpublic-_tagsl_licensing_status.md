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

# _tagSL_LICENSING_STATUS structure


## -description


Represents the licensing status.


## -struct-fields




### -field SkuId

Type: <b>SLID</b>

The SKU ID.


### -field eStatus

Type: <b><a href="https://msdn.microsoft.com/8af21021-ad18-4045-8a24-0af0d39db919">SLLICENSINGSTATUS</a></b>

The licensing status.


### -field dwGraceTime

Type: <b>DWORD</b>

The grace time in minutes.


### -field dwTotalGraceDays

Type: <b>DWORD</b>

The predefined grace days in the license.


### -field hrReason

Type: <b>HRESULT</b>

The error of unlicensed status.


### -field qwValidityExpiration

Type: <b>UINT64</b>

The validity expiration day.

