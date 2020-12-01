---
UID: NE:activationregistration.ThreadingType
title: ThreadingType (activationregistration.h)
description: Represents the apartment threading model to use for activating an in-process server.
helpviewer_keywords: ["ThreadingType","ThreadingType enumeration [Windows Runtime]","ThreadingType_BOTH","ThreadingType_MTA","ThreadingType_STA","activationregistration/ThreadingType","activationregistration/ThreadingType_BOTH","activationregistration/ThreadingType_MTA","activationregistration/ThreadingType_STA","winrt.threadingtype"]
old-location: winrt\threadingtype.htm
tech.root: WinRT
ms.assetid: D7D3A6D3-52DF-4634-A6FC-F5081E2E13B0
ms.date: 12/05/2018
ms.keywords: ThreadingType, ThreadingType enumeration [Windows Runtime], ThreadingType_BOTH, ThreadingType_MTA, ThreadingType_STA, activationregistration/ThreadingType, activationregistration/ThreadingType_BOTH, activationregistration/ThreadingType_MTA, activationregistration/ThreadingType_STA, winrt.threadingtype
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
req.typenames: ThreadingType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ThreadingType
 - activationregistration/ThreadingType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - activationregistration.h
api_name:
 - ThreadingType
---

# ThreadingType enumeration


## -description

Represents the apartment threading model to use for activating an in-process server.

## -enum-fields

### -field ThreadingType_BOTH

Apartment threading model is MTA and STA.

### -field ThreadingType_STA

Apartment threading model is STA.

### -field ThreadingType_MTA

Apartment threading model is MTA.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iactivatableclassregistration">IActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/nn-activationregistration-idllserveractivatableclassregistration">IDllServerActivatableClassRegistration</a>



<a href="/windows/desktop/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration">RoGetActivatableClassRegistration</a>