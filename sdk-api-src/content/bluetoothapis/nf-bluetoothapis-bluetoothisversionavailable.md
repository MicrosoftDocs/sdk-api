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

# BluetoothIsVersionAvailable function


## -description


The <b>BluetoothIsVersionAvailable</b> function indicates if the installed Bluetooth binary set supports      the requested version.


## -parameters




### -param MajorVersion [in]

The major version number.


### -param MinorVersion [in]

The minor version number.


## -returns



<b>TRUE</b> if the installed bluetooth binaries support the specified <i>MajorVersion</i> and <i>MinorVersion</i>; otherwise, <b>FALSE</b>.




## -remarks



This functionality is only exported in Bluetooth for Windows version 2.1 and later.



