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

# RtwqUnlockWorkQueue function


## -description


Unlocks a work queue.


## -parameters




### -param workQueueId [in]

Identifier for the work queue to be unlocked. This identifier is returned by the  <a href="https://msdn.microsoft.com/e2021bf3-40d8-4697-b82f-eebee2140a6e">RtwqAllocateSerialWorkQueue</a>, <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a>, or <a href="https://msdn.microsoft.com/ccebdbd8-fd3e-4e99-b1dd-1ec8e57cbff6">RtwqLockSharedWorkQueue</a> functions.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



