---
UID: NF:strmif.IAMDeviceRemoval.Disassociate
title: IAMDeviceRemoval::Disassociate
author: windows-sdk-content
description: The Disassociate method disassociates the KsProxy filter from the device by closing the device handle. The Filter Graph Manager calls this method if it receives a notification that the device was removed.
old-location: dshow\iamdeviceremoval_disassociate.htm
tech.root: DirectShow
ms.assetid: cf868f5d-3ec1-4c01-9154-27420d136fe5
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: Disassociate, Disassociate method [DirectShow], Disassociate method [DirectShow],IAMDeviceRemoval interface, IAMDeviceRemoval interface [DirectShow],Disassociate method, IAMDeviceRemoval.Disassociate, IAMDeviceRemoval::Disassociate, IAMDeviceRemovalDisassociate, dshow.iamdeviceremoval_disassociate, strmif/IAMDeviceRemoval::Disassociate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMDeviceRemoval::Disassociate


## -description



The <code>Disassociate</code> method disassociates the KsProxy filter from the device by closing the device handle. The Filter Graph Manager calls this method if it receives a notification that the device was removed.




## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3d67f577-9d85-47ca-b887-f259e9acc964">IAMDeviceRemoval Interface</a>
 

 

