---
UID: NF:activationregistration.IActivatableClassRegistration.get_RegistrationScope
title: IActivatableClassRegistration::get_RegistrationScope (activationregistration.h)
description: Gets the deployment scope of the current activatable class.
helpviewer_keywords: ["IActivatableClassRegistration interface [Windows Runtime]","get_RegistrationScope method","IActivatableClassRegistration.get_RegistrationScope","IActivatableClassRegistration::get_RegistrationScope","activationregistration/IActivatableClassRegistration::get_RegistrationScope","get_RegistrationScope","get_RegistrationScope method [Windows Runtime]","get_RegistrationScope method [Windows Runtime]","IActivatableClassRegistration interface","winrt.iactivatableclassregistration_registrationscope"]
old-location: winrt\iactivatableclassregistration_registrationscope.htm
tech.root: WinRT
ms.assetid: ACA72E3B-E559-4BE8-894F-A4D5F1FF3742
ms.date: 12/05/2018
ms.keywords: IActivatableClassRegistration interface [Windows Runtime],get_RegistrationScope method, IActivatableClassRegistration.get_RegistrationScope, IActivatableClassRegistration::get_RegistrationScope, activationregistration/IActivatableClassRegistration::get_RegistrationScope, get_RegistrationScope, get_RegistrationScope method [Windows Runtime], get_RegistrationScope method [Windows Runtime],IActivatableClassRegistration interface, winrt.iactivatableclassregistration_registrationscope
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
 - IActivatableClassRegistration::get_RegistrationScope
 - activationregistration/IActivatableClassRegistration::get_RegistrationScope
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
 - IActivatableClassRegistration.get_RegistrationScope
---

# IActivatableClassRegistration::get_RegistrationScope


## -description

Gets the deployment scope of the current activatable class.

## -parameters

### -param registrationScope [out, retval]

The deployment scope of the current activatable class.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iactivatableclassregistration">IActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/ne-activationregistration-registrationscope">RegistrationScope</a>



<a href="/windows/desktop/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration">RoGetActivatableClassRegistration</a>