---
UID: NF:activationregistration.IExeServerActivatableClassRegistration.get_ServerRegistration
title: IExeServerActivatableClassRegistration::get_ServerRegistration (activationregistration.h)
description: Gets the registration details for an out-of-process server.
helpviewer_keywords: ["IExeServerActivatableClassRegistration interface [Windows Runtime]","get_ServerRegistration method","IExeServerActivatableClassRegistration.get_ServerRegistration","IExeServerActivatableClassRegistration::get_ServerRegistration","activationregistration/IExeServerActivatableClassRegistration::get_ServerRegistration","get_ServerRegistration","get_ServerRegistration method [Windows Runtime]","get_ServerRegistration method [Windows Runtime]","IExeServerActivatableClassRegistration interface","winrt.iexeserveractivatableclassregistration_serverregistration"]
old-location: winrt\iexeserveractivatableclassregistration_serverregistration.htm
tech.root: WinRT
ms.assetid: 6116DC84-2DE0-427E-BDC7-425178B08C1A
ms.date: 12/05/2018
ms.keywords: IExeServerActivatableClassRegistration interface [Windows Runtime],get_ServerRegistration method, IExeServerActivatableClassRegistration.get_ServerRegistration, IExeServerActivatableClassRegistration::get_ServerRegistration, activationregistration/IExeServerActivatableClassRegistration::get_ServerRegistration, get_ServerRegistration, get_ServerRegistration method [Windows Runtime], get_ServerRegistration method [Windows Runtime],IExeServerActivatableClassRegistration interface, winrt.iexeserveractivatableclassregistration_serverregistration
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
 - IExeServerActivatableClassRegistration::get_ServerRegistration
 - activationregistration/IExeServerActivatableClassRegistration::get_ServerRegistration
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
 - IExeServerActivatableClassRegistration.get_ServerRegistration
---

# IExeServerActivatableClassRegistration::get_ServerRegistration


## -description

Gets the registration details for an out-of-process server.

## -parameters

### -param serverRegistration [out, retval]

The out-of-process server registration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration">IExeServerActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserverregistration">IExeServerRegistration</a>