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

# tagIMAGELISTSTATS structure


## -description


Contains image list statistics. Used by <a href="https://msdn.microsoft.com/D6402FCB-8E84-4F46-9B88-C0AFCEA66A9A">GetStatistics</a>.


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The image list size.


### -field cAlloc

Type: <b>int</b>

The number of images allocated.


### -field cUsed

Type: <b>int</b>

The number of images in use.


### -field cStandby

Type: <b>int</b>

The number of standby images.

