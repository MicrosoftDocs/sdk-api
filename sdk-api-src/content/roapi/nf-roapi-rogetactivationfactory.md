---
UID: NF:roapi.RoGetActivationFactory
title: RoGetActivationFactory function (roapi.h)
description: Gets the activation factory for the specified runtime class. (RoGetActivationFactory)
helpviewer_keywords: ["RoGetActivationFactory","RoGetActivationFactory function [Windows Runtime]","WinRTGetActivationFactory","roapi/RoGetActivationFactory","roapi/WinRTGetActivationFactory","winrt.rogetactivationfactory","winrt.winrtgetactivationfactory"]
old-location: winrt\rogetactivationfactory.htm
tech.root: WinRT
ms.assetid: 291ed35d-a459-4509-a265-89c49f8aa13a
ms.date: 12/05/2018
ms.keywords: RoGetActivationFactory, RoGetActivationFactory function [Windows Runtime], WinRTGetActivationFactory, roapi/RoGetActivationFactory, roapi/WinRTGetActivationFactory, winrt.rogetactivationfactory, winrt.winrtgetactivationfactory
req.header: roapi.h
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
req.lib: 
req.dll: Combase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoGetActivationFactory
 - roapi/RoGetActivationFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - combase.dll
 - API-MS-Win-Core-Winrt-l1-1-0.dll
 - api-ms-win-core-winrt-string-l1-1-0.dll
api_name:
 - RoGetActivationFactory
 - WinRTGetActivationFactory
---

# RoGetActivationFactory function


## -description

Gets the activation factory for the specified runtime class.

## -parameters

### -param activatableClassId [in]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a></b>

The ID of the activatable class.

### -param iid [in]

Type: <b>REFIID</b>

The reference ID of the interface.

### -param factory [out]

Type: <b>void**</b>

The activation factory.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
