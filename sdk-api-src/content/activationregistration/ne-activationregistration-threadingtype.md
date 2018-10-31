---
UID: NE:activationregistration.ThreadingType
title: ThreadingType
author: windows-sdk-content
description: Represents the apartment threading model to use for activating an in-process server.
old-location: winrt\threadingtype.htm
tech.root: WinRT
ms.assetid: D7D3A6D3-52DF-4634-A6FC-F5081E2E13B0
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ThreadingType, ThreadingType enumeration [Windows Runtime], ThreadingType_BOTH, ThreadingType_MTA, ThreadingType_STA, activationregistration/ThreadingType, activationregistration/ThreadingType_BOTH, activationregistration/ThreadingType_MTA, activationregistration/ThreadingType_STA, winrt.threadingtype
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
 - ThreadingType
product: Windows
targetos: Windows
req.typenames: ThreadingType
req.redist: 
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


### -field int




## -see-also




<a href="https://msdn.microsoft.com/99834A2D-547B-4B04-8703-46B11E0BB812">IActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/00E9476E-45E0-4D97-9DA4-FD293674BED4">IDllServerActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/9D9B74C9-9D9A-4E10-A222-C8F3658F2C48">RoGetActivatableClassRegistration</a>
 

 

