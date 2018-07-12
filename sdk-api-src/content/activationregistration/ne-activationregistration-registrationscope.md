---
UID: NE:activationregistration.RegistrationScope
title: RegistrationScope
author: windows-sdk-content
description: Represents the deployment scope of an activatable class.
old-location: winrt\registrationscope.htm
old-project: WinRT
ms.assetid: B4C14F6B-90BE-43AC-955B-229CDA025224
ms.author: windowssdkdev
ms.date: 07/06/2018
ms.keywords: InboxApp, PerMachine, PerUser, RegistrationScope, RegistrationScope enumeration [Windows Runtime], activationregistration/InboxApp, activationregistration/PerMachine, activationregistration/PerUser, activationregistration/RegistrationScope, winrt.registrationscope
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
req.idl: Activation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RegistrationScope
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
req.lib: 
req.dll: 
req.irql: 
---

# RegistrationScope enumeration


## -description


Represents the deployment scope of an activatable class.


## -enum-fields




### -field RegistrationScope_PerMachine


### -field RegistrationScope_PerUser


### -field RegistrationScope_InboxApp


### -field int




#### - InboxApp

Activation is per-machine, for a built-in app store.


#### - PerMachine

Activation is per-machine, for a Windows Store app.


#### - PerUser

Activation is per user, from a 3rd-party app store.


## -see-also




<a href="https://msdn.microsoft.com/99834A2D-547B-4B04-8703-46B11E0BB812">IActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/9D9B74C9-9D9A-4E10-A222-C8F3658F2C48">RoGetActivatableClassRegistration</a>
 

 

