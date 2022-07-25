---
UID: NF:activationregistration.IExeServerRegistration.get_Instancing
title: IExeServerRegistration::get_Instancing (activationregistration.h)
description: Gets the instancing behavior for the out-of-process server.
helpviewer_keywords: ["IExeServerRegistration interface [Windows Runtime]","get_Instancing method","IExeServerRegistration.get_Instancing","IExeServerRegistration::get_Instancing","activationregistration/IExeServerRegistration::get_Instancing","get_Instancing","get_Instancing method [Windows Runtime]","get_Instancing method [Windows Runtime]","IExeServerRegistration interface","winrt.iexeserverregistration_instancing"]
old-location: winrt\iexeserverregistration_instancing.htm
tech.root: WinRT
ms.assetid: 23618FBC-2404-4AB7-9842-7FD439F677B1
ms.date: 12/05/2018
ms.keywords: IExeServerRegistration interface [Windows Runtime],get_Instancing method, IExeServerRegistration.get_Instancing, IExeServerRegistration::get_Instancing, activationregistration/IExeServerRegistration::get_Instancing, get_Instancing, get_Instancing method [Windows Runtime], get_Instancing method [Windows Runtime],IExeServerRegistration interface, winrt.iexeserverregistration_instancing
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
 - IExeServerRegistration::get_Instancing
 - activationregistration/IExeServerRegistration::get_Instancing
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
 - IExeServerRegistration.get_Instancing
---

# IExeServerRegistration::get_Instancing


## -description

Gets the instancing behavior for the out-of-process server.

## -parameters

### -param instanceType [out, retval]

The instancing behavior for the out-of-process server.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration">IExeServerActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserverregistration">IExeServerRegistration</a>



<a href="/windows/desktop/api/activationregistration/ne-activationregistration-instancingtype">InstancingType</a>