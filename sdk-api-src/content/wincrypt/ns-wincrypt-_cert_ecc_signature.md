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

# _CERT_ECC_SIGNATURE structure


## -description


The <b>CERT_ECC_SIGNATURE</b> structure contains the r and s values for an Elliptic Curve Digital Signature Algorithm (ECDSA) signature.


## -struct-fields




### -field r

The r value of the ECDSA signature. This value is in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a> order.


### -field s

The s value of the ECDSA signature. This value is in little-endian order.


## -remarks



Before encoding, a leading zero byte will be inserted for the <b>r</b> and <b>s</b> members. After decoding, a leading zero byte will be removed from the <b>r</b> and <b>s</b> members if the leading zero is present.




