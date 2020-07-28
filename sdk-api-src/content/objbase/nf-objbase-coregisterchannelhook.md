---
UID: NF:objbase.CoRegisterChannelHook
title: CoRegisterChannelHook function (objbase.h)
description: Registers a channel hook.
helpviewer_keywords: ["CoRegisterChannelHook","CoRegisterChannelHook function [COM]","com.coregisterchannelhook","objbase/CoRegisterChannelHook"]
old-location: com\coregisterchannelhook.htm
tech.root: com
ms.assetid: 90281427-D0A3-4556-AF41-95DE7D000320
ms.date: 12/05/2018
ms.keywords: CoRegisterChannelHook, CoRegisterChannelHook function [COM], com.coregisterchannelhook, objbase/CoRegisterChannelHook
f1_keywords:
- objbase/CoRegisterChannelHook
dev_langs:
- c++
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
req.lib: Ole32.lib
req.dll: Combase.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- combase.dll
api_name:
- CoRegisterChannelHook
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



