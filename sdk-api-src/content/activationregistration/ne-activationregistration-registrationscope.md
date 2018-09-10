---
UID: NE:activationregistration.RegistrationScope
title: RegistrationScope
author: windows-sdk-content
description: Represents the deployment scope of an activatable class.
old-location: winrt\registrationscope.htm
tech.root: WinRT
ms.assetid: B4C14F6B-90BE-43AC-955B-229CDA025224
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RegistrationScope, RegistrationScope enumeration [Windows Runtime], RegistrationScope_InboxApp, RegistrationScope_PerMachine, RegistrationScope_PerUser, activationregistration/RegistrationScope, activationregistration/RegistrationScope_InboxApp, activationregistration/RegistrationScope_PerMachine, activationregistration/RegistrationScope_PerUser, winrt.registrationscope
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - activationregistration.h
api_name:
 - RegistrationScope
product: Windows
targetos: Windows
req.typenames: RegistrationScope
req.redist: 
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


### -field int




## -see-also




<a href="https://msdn.microsoft.com/99834A2D-547B-4B04-8703-46B11E0BB812">IActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/9D9B74C9-9D9A-4E10-A222-C8F3658F2C48">RoGetActivatableClassRegistration</a>
 

 

