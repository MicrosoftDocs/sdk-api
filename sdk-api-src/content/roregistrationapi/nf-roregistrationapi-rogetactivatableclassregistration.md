---
UID: NF:roregistrationapi.RoGetActivatableClassRegistration
title: RoGetActivatableClassRegistration function (roregistrationapi.h)
description: Enables retrieving class registration information.
helpviewer_keywords: ["RoGetActivatableClassRegistration","RoGetActivatableClassRegistration function [Windows Runtime]","roregistrationapi/RoGetActivatableClassRegistration","winrt.rogetactivatableclassregistration"]
old-location: winrt\rogetactivatableclassregistration.htm
tech.root: WinRT
ms.assetid: 9D9B74C9-9D9A-4E10-A222-C8F3658F2C48
ms.date: 12/05/2018
ms.keywords: RoGetActivatableClassRegistration, RoGetActivatableClassRegistration function [Windows Runtime], roregistrationapi/RoGetActivatableClassRegistration, winrt.rogetactivatableclassregistration
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
req.lib: Runtimeobject.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoGetActivatableClassRegistration
 - roregistrationapi/RoGetActivatableClassRegistration
dev_langs:
 - c++
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
---

# RoGetActivatableClassRegistration function


## -description

Enables retrieving class registration information.

## -parameters

### -param activatableClassId [in]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a></b>

The ID of the activatable class.

### -param activatableClassRegistration [out]

Type: <b>PActivatableClassRegistration*</b>

The registration information about the activatable class.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.