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

# IIOCancelInformation::SetCancelInformation


## -description


Sets information that is posted when a user selects <b>Cancel</b> from the progress UI. Allows the main object to tell the progress dialog thread about the process thread so that the progress dialog can send the process thread the message id when the user clicks <b>Cancel</b>.



## -parameters




### -param dwThreadID [in]

Type: <b>DWORD</b>

The ID of the process thread to be canceled.


### -param uMsgCancel [in]

Type: <b>UINT</b>

The cancel message to be posted to the thread.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 When the user selects <b>Cancel</b> from the progress UI, the <i>dwThreadID</i> will cancel any pending or future input/output (I/O) requests.  Also the <i>uMsgCancel</i> message, received from the progress dialog, will be posted to the thread to tell it to exit a wait state, if asynchronous I/O is pending.



