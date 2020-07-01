---
UID: NF:strmif.IAMDeviceRemoval.Disassociate
title: IAMDeviceRemoval::Disassociate (strmif.h)
description: The Disassociate method disassociates the KsProxy filter from the device by closing the device handle. The Filter Graph Manager calls this method if it receives a notification that the device was removed.
helpviewer_keywords: ["Disassociate","Disassociate method [DirectShow]","Disassociate method [DirectShow]","IAMDeviceRemoval interface","IAMDeviceRemoval interface [DirectShow]","Disassociate method","IAMDeviceRemoval.Disassociate","IAMDeviceRemoval::Disassociate","IAMDeviceRemovalDisassociate","dshow.iamdeviceremoval_disassociate","strmif/IAMDeviceRemoval::Disassociate"]
old-location: dshow\iamdeviceremoval_disassociate.htm
tech.root: DirectShow
ms.assetid: cf868f5d-3ec1-4c01-9154-27420d136fe5
ms.date: 12/05/2018
ms.keywords: Disassociate, Disassociate method [DirectShow], Disassociate method [DirectShow],IAMDeviceRemoval interface, IAMDeviceRemoval interface [DirectShow],Disassociate method, IAMDeviceRemoval.Disassociate, IAMDeviceRemoval::Disassociate, IAMDeviceRemovalDisassociate, dshow.iamdeviceremoval_disassociate, strmif/IAMDeviceRemoval::Disassociate
f1_keywords:
- strmif/IAMDeviceRemoval.Disassociate
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMDeviceRemoval.Disassociate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDeviceRemoval::Disassociate


## -description



The <code>Disassociate</code> method disassociates the KsProxy filter from the device by closing the device handle. The Filter Graph Manager calls this method if it receives a notification that the device was removed.




## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamdeviceremoval">IAMDeviceRemoval Interface</a>
 

 

