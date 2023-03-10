---
UID: NF:activationregistration.IDllServerActivatableClassRegistration.get_ThreadingType
title: IDllServerActivatableClassRegistration::get_ThreadingType (activationregistration.h)
description: Gets the apartment threading model for activating the in-process server.
helpviewer_keywords: ["IDllServerActivatableClassRegistration interface [Windows Runtime]","get_ThreadingType method","IDllServerActivatableClassRegistration.get_ThreadingType","IDllServerActivatableClassRegistration::get_ThreadingType","activationregistration/IDllServerActivatableClassRegistration::get_ThreadingType","get_ThreadingType","get_ThreadingType method [Windows Runtime]","get_ThreadingType method [Windows Runtime]","IDllServerActivatableClassRegistration interface","winrt.idllserveractivatableclassregistration_threadingtype"]
old-location: winrt\idllserveractivatableclassregistration_threadingtype.htm
tech.root: WinRT
ms.assetid: 08F95AD6-B559-4652-A496-84777BF0189D
ms.date: 12/05/2018
ms.keywords: IDllServerActivatableClassRegistration interface [Windows Runtime],get_ThreadingType method, IDllServerActivatableClassRegistration.get_ThreadingType, IDllServerActivatableClassRegistration::get_ThreadingType, activationregistration/IDllServerActivatableClassRegistration::get_ThreadingType, get_ThreadingType, get_ThreadingType method [Windows Runtime], get_ThreadingType method [Windows Runtime],IDllServerActivatableClassRegistration interface, winrt.idllserveractivatableclassregistration_threadingtype
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
 - IDllServerActivatableClassRegistration::get_ThreadingType
 - activationregistration/IDllServerActivatableClassRegistration::get_ThreadingType
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
 - IDllServerActivatableClassRegistration.get_ThreadingType
---

# IDllServerActivatableClassRegistration::get_ThreadingType


## -description

Gets the apartment threading model for activating the in-process server.

## -parameters

### -param threadingType [out, retval]

The apartment threading model for the in-process server.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-idllserveractivatableclassregistration">IDllServerActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/ne-activationregistration-threadingtype">ThreadingType</a>