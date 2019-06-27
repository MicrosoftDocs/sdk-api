---
UID: NF:wcndevice.IWCNDevice.Unadvise
title: IWCNDevice::Unadvise (wcndevice.h)
author: windows-sdk-content
description: IWCNDevice::Unadvise method removes any callback previously set via IWCNDevice::Connect.
old-location: wcn\iwcndevice_unadvise.htm
tech.root: wcn
ms.assetid: d76ebc9e-8adc-4640-a377-f69cef43afca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWCNDevice interface [Windows Connect Now],Unadvise method, IWCNDevice.Unadvise, IWCNDevice::Unadvise, Unadvise, Unadvise method [Windows Connect Now], Unadvise method [Windows Connect Now],IWCNDevice interface, wcn.iwcndevice_unadvise, wcndevice/IWCNDevice::Unadvise
ms.topic: method
f1_keywords: 
 - "wcndevice/IWCNDevice.Unadvise"
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
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
 - WcnDevice.h
api_name:
 - IWCNDevice.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWCNDevice::Unadvise


## -description


The <b>IWCNDevice::Unadvise</b> method removes any callback previously set via <a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a>.


## -parameters






## -returns



This method does not return a value.




## -remarks



It is not necessary to call <b>IWCNDevice::Unadvise</b> unless the application is shutting down and must ensure that no more callbacks are received on its <a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nn-wcndevice-iwcnconnectnotify">IWCNConnectNotify</a> callback.
Do not call <b>IWCNDevice::Unadvise</b> from within an <b>IWCNConnectNotify</b> callback, since that will cause a deadlock.
Note that <b>IWCNDevice::Unadvise</b> does not cancel the connect operation on the wire.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nn-wcndevice-iwcnconnectnotify">IWCNConnectNotify</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a>
 

 

