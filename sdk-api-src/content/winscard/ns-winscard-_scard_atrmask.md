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

# _SCARD_ATRMASK structure


## -description


The <b>SCARD_ATRMASK</b> structure is used by 
the <a href="https://msdn.microsoft.com/6c4a644c-033f-4654-b96d-0379e9ac0bb4">SCardLocateCardsByATR</a> function to locate cards.


## -struct-fields




### -field cbAtr

The number of bytes in the ATR and the mask.


### -field rgbAtr

An array of <b>BYTE</b> values for the ATR of the card with extra alignment bytes.


### -field rgbMask

An array of <b>BYTE</b> values for the mask for the ATR with extra alignment bytes.

