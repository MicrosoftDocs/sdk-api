---
UID: NF:roregistrationapi.RoGetActivatableClassRegistration
title: RoGetActivatableClassRegistration function
author: windows-sdk-content
description: Enables retrieving class registration information.
old-location: winrt\rogetactivatableclassregistration.htm
old-project: WinRT
ms.assetid: 9D9B74C9-9D9A-4E10-A222-C8F3658F2C48
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: RoGetActivatableClassRegistration, RoGetActivatableClassRegistration function [Windows Runtime], roregistrationapi/RoGetActivatableClassRegistration, winrt.rogetactivatableclassregistration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: roregistrationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - runtimeobject.lib
 - runtimeobject.dll
 - API-MS-Win-Core-WinRT-registration-l1-1-0.dll
 - ComBase.dll
api_name:
 - RoGetActivatableClassRegistration
product: Windows
targetos: Windows
req.lib: Runtimeobject.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# RoGetActivatableClassRegistration function


## -description


Enables retrieving class registration information.


## -parameters




### -param activatableClassId [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The ID of the activatable class.


### -param activatableClassRegistration [out]

Type: <b>PActivatableClassRegistration*</b>

The registration information about the activatable class.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



