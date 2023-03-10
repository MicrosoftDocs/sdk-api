---
UID: NE:activationregistration.InstancingType
title: InstancingType (activationregistration.h)
description: Represents the kind of instancing behavior for the out-of-process server.
helpviewer_keywords: ["InstancingType","InstancingType enumeration [Windows Runtime]","InstancingType_MultipleInstances","InstancingType_SingleInstance","activationregistration/InstancingType","activationregistration/InstancingType_MultipleInstances","activationregistration/InstancingType_SingleInstance","winrt.instancingtype"]
old-location: winrt\instancingtype.htm
tech.root: WinRT
ms.assetid: 42E6A5EE-06B0-4F38-92D0-729922AD9FFF
ms.date: 12/05/2018
ms.keywords: InstancingType, InstancingType enumeration [Windows Runtime], InstancingType_MultipleInstances, InstancingType_SingleInstance, activationregistration/InstancingType, activationregistration/InstancingType_MultipleInstances, activationregistration/InstancingType_SingleInstance, winrt.instancingtype
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
req.typenames: InstancingType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InstancingType
 - activationregistration/InstancingType
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
 - InstancingType
---

# InstancingType enumeration


## -description

Represents the kind of  instancing behavior for the out-of-process server.

## -enum-fields

### -field InstancingType_SingleInstance

Create a singleton instance of the out-of-process server.

### -field InstancingType_MultipleInstances

Create more than one instance of the out-of-process server.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration">IExeServerActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserverregistration">IExeServerRegistration</a>