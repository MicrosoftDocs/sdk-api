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

# IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo


## -description


Retrieves the <a href="https://msdn.microsoft.com/18f9260d-b7cd-4b45-a7bd-f3bd3647eebe">IMILBitmapEffectConnectorInfo</a> associated with the given output pin.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which output pin to query for connector information.


### -param ppConnectorInfo [out]

Type: <b><a href="https://msdn.microsoft.com/18f9260d-b7cd-4b45-a7bd-f3bd3647eebe">IMILBitmapEffectConnectorInfo</a>**</b>

When this method returns, contain the connector information for the given output pin.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



