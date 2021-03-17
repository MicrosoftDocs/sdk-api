---
UID: NE:activationregistration.RegistrationScope
title: RegistrationScope (activationregistration.h)
description: Represents the deployment scope of an activatable class.
helpviewer_keywords: ["RegistrationScope","RegistrationScope enumeration [Windows Runtime]","RegistrationScope_InboxApp","RegistrationScope_PerMachine","RegistrationScope_PerUser","activationregistration/RegistrationScope","activationregistration/RegistrationScope_InboxApp","activationregistration/RegistrationScope_PerMachine","activationregistration/RegistrationScope_PerUser","winrt.registrationscope"]
old-location: winrt\registrationscope.htm
tech.root: WinRT
ms.assetid: B4C14F6B-90BE-43AC-955B-229CDA025224
ms.date: 12/05/2018
ms.keywords: RegistrationScope, RegistrationScope enumeration [Windows Runtime], RegistrationScope_InboxApp, RegistrationScope_PerMachine, RegistrationScope_PerUser, activationregistration/RegistrationScope, activationregistration/RegistrationScope_InboxApp, activationregistration/RegistrationScope_PerMachine, activationregistration/RegistrationScope_PerUser, winrt.registrationscope
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
req.typenames: RegistrationScope
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegistrationScope
 - activationregistration/RegistrationScope
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
 - RegistrationScope
---

# RegistrationScope enumeration


## -description

Represents the deployment scope of an activatable class.

## -enum-fields

### -field RegistrationScope_PerMachine

Activation is per-machine, for a Windows Store app.

### -field RegistrationScope_PerUser

Activation is per user, from a 3rd-party app store.

### -field RegistrationScope_InboxApp

Activation is per-machine, for a built-in app store.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iactivatableclassregistration">IActivatableClassRegistration</a>



<a href="/windows/desktop/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration">RoGetActivatableClassRegistration</a>