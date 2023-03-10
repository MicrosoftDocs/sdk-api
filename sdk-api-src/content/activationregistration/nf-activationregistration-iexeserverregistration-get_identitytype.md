---
UID: NF:activationregistration.IExeServerRegistration.get_IdentityType
title: IExeServerRegistration::get_IdentityType (activationregistration.h)
description: Gets the activation type for the out-of-process server.
helpviewer_keywords: ["IExeServerRegistration interface [Windows Runtime]","get_IdentityType method","IExeServerRegistration.get_IdentityType","IExeServerRegistration::get_IdentityType","activationregistration/IExeServerRegistration::get_IdentityType","get_IdentityType","get_IdentityType method [Windows Runtime]","get_IdentityType method [Windows Runtime]","IExeServerRegistration interface","winrt.iexeserverregistration_identitytype"]
old-location: winrt\iexeserverregistration_identitytype.htm
tech.root: WinRT
ms.assetid: DF0A20D8-5028-4A7B-B8E6-CAF5C3716407
ms.date: 12/05/2018
ms.keywords: IExeServerRegistration interface [Windows Runtime],get_IdentityType method, IExeServerRegistration.get_IdentityType, IExeServerRegistration::get_IdentityType, activationregistration/IExeServerRegistration::get_IdentityType, get_IdentityType, get_IdentityType method [Windows Runtime], get_IdentityType method [Windows Runtime],IExeServerRegistration interface, winrt.iexeserverregistration_identitytype
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
 - IExeServerRegistration::get_IdentityType
 - activationregistration/IExeServerRegistration::get_IdentityType
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
 - IExeServerRegistration.get_IdentityType
---

# IExeServerRegistration::get_IdentityType


## -description

Gets the activation type for the out-of-process server.

## -parameters

### -param identityType [out, retval]

The activation type.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration">IExeServerActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserverregistration">IExeServerRegistration</a>



<a href="/windows/desktop/api/activationregistration/ne-activationregistration-identitytype">IdentityType</a>