---
UID: NF:activationregistration.IActivatableClassRegistration.get_ActivationType
title: IActivatableClassRegistration::get_ActivationType (activationregistration.h)
description: Gets the kind of activation for the current activatable class.
helpviewer_keywords: ["IActivatableClassRegistration interface [Windows Runtime]","get_ActivationType method","IActivatableClassRegistration.get_ActivationType","IActivatableClassRegistration::get_ActivationType","activationregistration/IActivatableClassRegistration::get_ActivationType","get_ActivationType","get_ActivationType method [Windows Runtime]","get_ActivationType method [Windows Runtime]","IActivatableClassRegistration interface","winrt.iactivatableclassregistration_activationtype"]
old-location: winrt\iactivatableclassregistration_activationtype.htm
tech.root: WinRT
ms.assetid: 145DF7F2-839A-4B94-B4DC-BA2103A04D2F
ms.date: 12/05/2018
ms.keywords: IActivatableClassRegistration interface [Windows Runtime],get_ActivationType method, IActivatableClassRegistration.get_ActivationType, IActivatableClassRegistration::get_ActivationType, activationregistration/IActivatableClassRegistration::get_ActivationType, get_ActivationType, get_ActivationType method [Windows Runtime], get_ActivationType method [Windows Runtime],IActivatableClassRegistration interface, winrt.iactivatableclassregistration_activationtype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActivatableClassRegistration::get_ActivationType
 - activationregistration/IActivatableClassRegistration::get_ActivationType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - activationregistration.h
api_name:
 - IActivatableClassRegistration.get_ActivationType
---

# IActivatableClassRegistration::get_ActivationType


## -description

Gets the kind of activation for the current activatable class.

## -parameters

### -param activationType [out, retval]

The kind of activation for the current activatable class.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/ne-activationregistration-activationtype">ActivationType</a>



<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iactivatableclassregistration">IActivatableClassRegistration</a>



<a href="/windows/desktop/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration">RoGetActivatableClassRegistration</a>