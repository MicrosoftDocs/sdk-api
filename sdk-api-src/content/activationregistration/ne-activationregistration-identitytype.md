---
UID: NE:activationregistration.IdentityType
title: IdentityType
author: windows-sdk-content
description: Represents the kind of activation for an out-of-process server.
old-location: winrt\identitytype.htm
tech.root: WinRT
ms.assetid: 17EBFEE2-903A-4B64-A59F-D94E96E4457E
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IdentityType, IdentityType enumeration [Windows Runtime], IdentityType_ActivateAsActivatingUser, IdentityType_ActivateAsActivator, IdentityType_ActivateAsPackage, IdentityType_RunAs, IdentityType_SessionUser, IdentityType_SessionVirtual, activationregistration/IdentityType, activationregistration/IdentityType_ActivateAsActivatingUser, activationregistration/IdentityType_ActivateAsActivator, activationregistration/IdentityType_ActivateAsPackage, activationregistration/IdentityType_RunAs, activationregistration/IdentityType_SessionUser, activationregistration/IdentityType_SessionVirtual, winrt.identitytype
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
 - IdentityType
product: Windows
targetos: Windows
req.typenames: IdentityType
req.redist: 
---

# IdentityType enumeration


## -description


Represents the kind of activation for an out-of-process server.


## -enum-fields




### -field IdentityType_ActivateAsActivator

Activate the out-of-process server as an activator.


### -field IdentityType_RunAs

Activate the out-of-process server as an executable.


### -field IdentityType_ActivateAsPackage

Activate the out-of-process server as a Windows Store app package.


### -field IdentityType_SessionVirtual

Activate the out-of-process server as a virtual session.


### -field IdentityType_SessionUser

Activate the out-of-process server as a user session.


### -field IdentityType_ActivateAsActivatingUser

Activate the out-of-process server as an activating user.


### -field int




## -see-also




<a href="https://msdn.microsoft.com/1D8F7B12-2883-478D-B83D-84AC47D512E4">IExeServerActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/9A96968D-B9BD-4C47-B626-69B6EA6AE7EA">IExeServerRegistration</a>
 

 

