---
UID: NF:objbase.CoRegisterChannelHook
title: CoRegisterChannelHook function
author: windows-driver-content
description: Registers a channel hook.
old-location: com\coregisterchannelhook.htm
old-project: com
ms.assetid: 90281427-D0A3-4556-AF41-95DE7D000320
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: CoRegisterChannelHook, CoRegisterChannelHook function [COM], com.coregisterchannelhook, objbase/CoRegisterChannelHook
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COMSD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	combase.dll
api_name:
-	CoRegisterChannelHook
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Combase.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CoRegisterChannelHook function


## -description


Registers a channel hook.


## -parameters




### -param ExtensionUuid [in]

The extension to register.


### -param pChannelHook [in]

The channel hook to register.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



