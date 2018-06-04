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

# WTS_CERT_TYPE enumeration


## -description


Contains values that specify the type of certificate used to obtain a license.


## -enum-fields




### -field WTS_CERT_TYPE_INVALID

The certificate is not valid.


### -field WTS_CERT_TYPE_PROPRIETORY

The certificate is a custom type.


### -field WTS_CERT_TYPE_X509

The certificate adheres to the X.509 standard.


## -remarks



This enumeration is used by the <a href="https://msdn.microsoft.com/975a534e-03f1-4c8f-9de1-42144e31c8cb">WTS_LICENSE_CAPABILITIES</a> structure.



