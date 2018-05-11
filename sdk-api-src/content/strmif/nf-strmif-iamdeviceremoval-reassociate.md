---
UID: NF:strmif.IAMDeviceRemoval.Reassociate
title: IAMDeviceRemoval::Reassociate
author: windows-driver-content
description: The Reassociate method reassociates the KsProxy filter with the device. The Filter Graph Manager calls this method if it receives a notification that the device has returned after being removed.
old-location: dshow\iamdeviceremoval_reassociate.htm
old-project: DirectShow
ms.assetid: 214b98c7-4143-4466-a359-1e9c9e4c778d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IAMDeviceRemoval interface [DirectShow],Reassociate method, IAMDeviceRemoval.Reassociate, IAMDeviceRemoval::Reassociate, IAMDeviceRemovalReassociate, Reassociate, Reassociate method [DirectShow], Reassociate method [DirectShow],IAMDeviceRemoval interface, dshow.iamdeviceremoval_reassociate, strmif/IAMDeviceRemoval::Reassociate
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMDeviceRemoval.Reassociate
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMDeviceRemoval::Reassociate


## -description



The <code>Reassociate</code> method reassociates the KsProxy filter with the device. The Filter Graph Manager calls this method if it receives a notification that the device has returned after being removed.




## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3d67f577-9d85-47ca-b887-f259e9acc964">IAMDeviceRemoval Interface</a>
 

 

