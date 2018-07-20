---
UID: NE:activationregistration.IdentityType
title: IdentityType
author: windows-sdk-content
description: Represents the kind of activation for an out-of-process server.
old-location: winrt\identitytype.htm
old-project: WinRT
ms.assetid: 17EBFEE2-903A-4B64-A59F-D94E96E4457E
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ActivateAsActivator, ActivateAsPackage, IdentityType, IdentityType enumeration [Windows Runtime], RunAs, activationregistration/ActivateAsActivator, activationregistration/ActivateAsPackage, activationregistration/IdentityType, activationregistration/RunAs, winrt.identitytype
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
req.typenames: IdentityType
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
req.lib: 
req.dll: 
req.irql: 
---

# IdentityType enumeration


## -description


Represents the kind of activation for an out-of-process server.


## -enum-fields




### -field IdentityType_ActivateAsActivator


### -field IdentityType_RunAs


### -field IdentityType_ActivateAsPackage


### -field IdentityType_SessionVirtual


### -field IdentityType_SessionUser


### -field IdentityType_ActivateAsActivatingUser


### -field int




#### - ActivateAsActivator

Activate the out-of-process server as an activator.


#### - ActivateAsPackage

Activate the out-of-process server as a Windows Store app package.


#### - RunAs

Activate the out-of-process server as an executable.


## -see-also




<a href="https://msdn.microsoft.com/1D8F7B12-2883-478D-B83D-84AC47D512E4">IExeServerActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/9A96968D-B9BD-4C47-B626-69B6EA6AE7EA">IExeServerRegistration</a>
 

 

