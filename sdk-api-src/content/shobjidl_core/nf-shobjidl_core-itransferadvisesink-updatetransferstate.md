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

# ITransferAdviseSink::UpdateTransferState


## -description


Updates the transfer state.


## -parameters




### -param ts [in]

Type: <b>TRANSFER_ADVISE_STATE</b>

The transfer state. One of the following values.



#### TS_NONE (0x00000000)

0x00000000. No transfer is in progress.



#### TS_PERFORMING (0x00000001)

0x00000001. The transfer is being performed.



#### TS_PREPARING (0x00000002)

0x00000002. The transfer is preparing to begin. For example, this flag would be set when space requirements are being calculated.



#### TS_INDETERMINATE (0x00000004)

0x00000004. Length of the transfer is unknown.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



