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

# IIOCancelInformation::GetCancelInformation


## -description


Returns information that is posted when a user selects <b>Cancel</b> from the progress UI. The process thread uses this method to find out which message the progress dialog will send to the process thread when the user hits cancel.  The process thread then listens for this message and does its own cleanup upon receipt.



## -parameters




### -param pdwThreadID [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to the ID of the process thread.


### -param puMsgCancel [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to <i>uMsgCancel</i> that the process thread should post if the operation is canceled.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



