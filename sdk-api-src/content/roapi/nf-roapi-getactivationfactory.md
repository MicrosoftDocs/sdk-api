---
UID: NF:roapi.GetActivationFactory
title: GetActivationFactory function (roapi.h)
description: Gets the activation factory for the specified runtime class. (WinRTGetActivationFactory)
helpviewer_keywords: ["GetActivationFactory","GetActivationFactory function [Windows Runtime]","WinRTGetActivationFactory","roapi/GetActivationFactory","roapi/WinRTGetActivationFactory","winrt.getactivationfactory"]
old-location: winrt\getactivationfactory.htm
tech.root: WinRT
ms.assetid: FD1A62C6-069E-40D1-A009-78C157E08F20
ms.date: 12/05/2018
ms.keywords: GetActivationFactory, GetActivationFactory function [Windows Runtime], WinRTGetActivationFactory, roapi/GetActivationFactory, roapi/WinRTGetActivationFactory, winrt.getactivationfactory
req.header: roapi.h
req.include-header: Stdafx.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - GetActivationFactory
 - roapi/GetActivationFactory
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
api_name:
 - GetActivationFactory
 - WinRTGetActivationFactory
---

# GetActivationFactory function


## -description

Gets the activation factory for the specified runtime class.

## -parameters

### -param activatableClassId [in]

The ID of the activatable class.

### -param factory [out]

The activation factory.

### -param unnamedParam3

TBD

## -returns

Returns S_OK on success.

