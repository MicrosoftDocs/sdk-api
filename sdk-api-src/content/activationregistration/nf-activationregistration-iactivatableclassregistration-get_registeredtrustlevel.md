---
UID: NF:activationregistration.IActivatableClassRegistration.get_RegisteredTrustLevel
title: IActivatableClassRegistration::get_RegisteredTrustLevel (activationregistration.h)
description: Gets the trust level of the current activatable class.
helpviewer_keywords: ["IActivatableClassRegistration interface [Windows Runtime]","get_RegisteredTrustLevel method","IActivatableClassRegistration.get_RegisteredTrustLevel","IActivatableClassRegistration::get_RegisteredTrustLevel","activationregistration/IActivatableClassRegistration::get_RegisteredTrustLevel","get_RegisteredTrustLevel","get_RegisteredTrustLevel method [Windows Runtime]","get_RegisteredTrustLevel method [Windows Runtime]","IActivatableClassRegistration interface","winrt.iactivatableclassregistration_registeredtrustlevel"]
old-location: winrt\iactivatableclassregistration_registeredtrustlevel.htm
tech.root: WinRT
ms.assetid: 3DFE773C-CF63-489A-988B-2FFF4215C8BF
ms.date: 12/05/2018
ms.keywords: IActivatableClassRegistration interface [Windows Runtime],get_RegisteredTrustLevel method, IActivatableClassRegistration.get_RegisteredTrustLevel, IActivatableClassRegistration::get_RegisteredTrustLevel, activationregistration/IActivatableClassRegistration::get_RegisteredTrustLevel, get_RegisteredTrustLevel, get_RegisteredTrustLevel method [Windows Runtime], get_RegisteredTrustLevel method [Windows Runtime],IActivatableClassRegistration interface, winrt.iactivatableclassregistration_registeredtrustlevel
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
 - IActivatableClassRegistration::get_RegisteredTrustLevel
 - activationregistration/IActivatableClassRegistration::get_RegisteredTrustLevel
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
 - IActivatableClassRegistration.get_RegisteredTrustLevel
---

# IActivatableClassRegistration::get_RegisteredTrustLevel


## -description

Gets the trust level of the current activatable class.

## -parameters

### -param registeredTrustLevel [out, retval]

The trust level of the current activatable class.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iactivatableclassregistration">IActivatableClassRegistration</a>



<a href="/previous-versions/dn408470(v=vs.85)">RegisteredTrustLevel</a>



<a href="/windows/desktop/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration">RoGetActivatableClassRegistration</a>