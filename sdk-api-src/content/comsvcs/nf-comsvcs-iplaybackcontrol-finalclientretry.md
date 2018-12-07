---
UID: NF:comsvcs.IPlaybackControl.FinalClientRetry
title: IPlaybackControl::FinalClientRetry
author: windows-sdk-content
description: Informs the client-side exception handling component that all Message Queuing attempts to deliver the message to the server were rejected. The message ended up on the client-side Xact dead letter queue.
old-location: cos\iplaybackcontrol_finalclientretry.htm
tech.root: cossdk
ms.assetid: 3fa51832-0e68-4e76-bbdb-ce54f76fbae6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FinalClientRetry, FinalClientRetry method [COM+], FinalClientRetry method [COM+],IPlaybackControl interface, IPlaybackControl interface [COM+],FinalClientRetry method, IPlaybackControl.FinalClientRetry, IPlaybackControl::FinalClientRetry, _cos_IPlaybackControl_FinalClientRetry, comsvcs/IPlaybackControl::FinalClientRetry, cos.iplaybackcontrol_finalclientretry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IPlaybackControl.FinalClientRetry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPlaybackControl::FinalClientRetry


## -description


Informs the client-side exception handling component that all Message Queuing attempts to deliver the message to the server were rejected. The message ended up on the client-side Xact dead letter queue.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



As messages arrive on the Xact dead letter queue, COM+ attempts to invoke a client-side exception handler related to the server class to deliver this notification. This exception object might take exceptional action, such as recording the failure, sending a mail message to the administrator, or taking client-side compensating action (reversing the effect of an earlier transaction).



If this method is not successful, the message is left on the Xact dead letter queue.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680150(v=VS.85).aspx">IPlaybackControl</a>
 

 

