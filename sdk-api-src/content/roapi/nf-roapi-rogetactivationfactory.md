---
UID: NF:roapi.RoGetActivationFactory
title: RoGetActivationFactory function
author: windows-sdk-content
description: Gets the activation factory for the specified runtime class.
old-location: winrt\rogetactivationfactory.htm
old-project: WinRT
ms.assetid: 291ed35d-a459-4509-a265-89c49f8aa13a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: RoGetActivationFactory, RoGetActivationFactory function [Windows Runtime], WinRTGetActivationFactory, roapi/RoGetActivationFactory, roapi/WinRTGetActivationFactory, winrt.rogetactivationfactory, winrt.winrtgetactivationfactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: RO_INIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - combase.dll
 - API-MS-Win-Core-Winrt-l1-1-0.dll
api_name:
 - RoGetActivationFactory
 - WinRTGetActivationFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: Combase.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RoGetActivationFactory function


## -description


Gets the activation factory for the specified runtime class.


## -parameters




### -param activatableClassId [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The ID of the activatable class.


### -param iid [in]

Type: <b>REFIID</b>

The reference ID of the interface.


### -param factory [out]

Type: <b>void**</b>

The activation factory.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



