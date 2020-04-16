---
UID: NF:activationregistration.IActivatableClassRegistration.get_ActivatableClassId
title: IActivatableClassRegistration::get_ActivatableClassId (activationregistration.h)
description: Gets the class identifier for the current activatable class.helpviewer_keywords: ["IActivatableClassRegistration interface [Windows Runtime]","get_ActivatableClassId method","IActivatableClassRegistration.get_ActivatableClassId","IActivatableClassRegistration::get_ActivatableClassId","activationregistration/IActivatableClassRegistration::get_ActivatableClassId","get_ActivatableClassId","get_ActivatableClassId method [Windows Runtime]","get_ActivatableClassId method [Windows Runtime]","IActivatableClassRegistration interface","winrt.iactivatableclassregistration_activatableclassid"]
old-location: winrt\iactivatableclassregistration_activatableclassid.htm
tech.root: WinRT
ms.assetid: 8AE55B74-8AC3-4F13-8FEE-7C3C52DEE96F
ms.date: 12/05/2018
ms.keywords: IActivatableClassRegistration interface [Windows Runtime],get_ActivatableClassId method, IActivatableClassRegistration.get_ActivatableClassId, IActivatableClassRegistration::get_ActivatableClassId, activationregistration/IActivatableClassRegistration::get_ActivatableClassId, get_ActivatableClassId, get_ActivatableClassId method [Windows Runtime], get_ActivatableClassId method [Windows Runtime],IActivatableClassRegistration interface, winrt.iactivatableclassregistration_activatableclassid
f1_keywords:
- activationregistration/IActivatableClassRegistration.get_ActivatableClassId
dev_langs:
- c++
req.header: activationregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
- activationregistration.h
api_name:
- IActivatableClassRegistration.get_ActivatableClassId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActivatableClassRegistration::get_ActivatableClassId


## -description


Gets the class identifier for the current activatable class.


## -parameters




### -param activatableClassID [out, retval]

The identifier for the current activatable class.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>



<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nn-activationregistration-iactivatableclassregistration">IActivatableClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration">RoGetActivatableClassRegistration</a>
 

 

