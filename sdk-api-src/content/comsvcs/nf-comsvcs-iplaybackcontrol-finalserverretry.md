---
UID: NF:comsvcs.IPlaybackControl.FinalServerRetry
title: IPlaybackControl::FinalServerRetry (comsvcs.h)
description: Informs the server-side Exception_CLSID implementation that all attempts to play back the deferred activation have failed. The message is about to be moved to the final resting queue.
helpviewer_keywords: ["FinalServerRetry","FinalServerRetry method [COM+]","FinalServerRetry method [COM+]","IPlaybackControl interface","IPlaybackControl interface [COM+]","FinalServerRetry method","IPlaybackControl.FinalServerRetry","IPlaybackControl::FinalServerRetry","_cos_IPlaybackControl_FinalServerRetry","comsvcs/IPlaybackControl::FinalServerRetry","cos.iplaybackcontrol_finalserverretry"]
old-location: cos\iplaybackcontrol_finalserverretry.htm
tech.root: cos
ms.assetid: 03f0bd46-004d-4ed6-b00b-de765d339ba0
ms.date: 12/05/2018
ms.keywords: FinalServerRetry, FinalServerRetry method [COM+], FinalServerRetry method [COM+],IPlaybackControl interface, IPlaybackControl interface [COM+],FinalServerRetry method, IPlaybackControl.FinalServerRetry, IPlaybackControl::FinalServerRetry, _cos_IPlaybackControl_FinalServerRetry, comsvcs/IPlaybackControl::FinalServerRetry, cos.iplaybackcontrol_finalserverretry
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPlaybackControl::FinalServerRetry
 - comsvcs/IPlaybackControl::FinalServerRetry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IPlaybackControl.FinalServerRetry
---

# IPlaybackControl::FinalServerRetry


## -description

Informs the server-side Exception_CLSID implementation that all attempts to play back the deferred activation have failed. The message is about to be moved to the final resting queue.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

As the message is about to be moved to the final resting queue, the server object may attempt to record the failure, send a mail message to the administrator, or take client-side compensating action (reversing the effect of an earlier transaction). The server object should make every effort to complete this transaction successfully. Otherwise, manual intervention is required to reprocess the message.



If this method is not successful, the message is moved to the final resting queue.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iplaybackcontrol">IPlaybackControl</a>
