---
UID: NF:mileffects.IMILBitmapEffectConnections.GetOutputConnector
title: IMILBitmapEffectConnections::GetOutputConnector (mileffects.h)
description: Retrieves the output connector associated with the given pin index.
helpviewer_keywords: ["GetOutputConnector","GetOutputConnector method [WPF Bitmap Effects]","GetOutputConnector method [WPF Bitmap Effects]","IMILBitmapEffectConnections interface","IMILBitmapEffectConnections interface [WPF Bitmap Effects]","GetOutputConnector method","IMILBitmapEffectConnections.GetOutputConnector","IMILBitmapEffectConnections::GetOutputConnector","_wibe_imilbitmapeffectconnections_getoutputconnector","mileffects/IMILBitmapEffectConnections::GetOutputConnector","wibe._wibe_imilbitmapeffectconnections_getoutputconnector"]
old-location: wibe\_wibe_imilbitmapeffectconnections_getoutputconnector.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnections\getoutputconnector.htm
ms.date: 12/05/2018
ms.keywords: GetOutputConnector, GetOutputConnector method [WPF Bitmap Effects], GetOutputConnector method [WPF Bitmap Effects],IMILBitmapEffectConnections interface, IMILBitmapEffectConnections interface [WPF Bitmap Effects],GetOutputConnector method, IMILBitmapEffectConnections.GetOutputConnector, IMILBitmapEffectConnections::GetOutputConnector, _wibe_imilbitmapeffectconnections_getoutputconnector, mileffects/IMILBitmapEffectConnections::GetOutputConnector, wibe._wibe_imilbitmapeffectconnections_getoutputconnector
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
f1_keywords:
 - IMILBitmapEffectConnections::GetOutputConnector
 - mileffects/IMILBitmapEffectConnections::GetOutputConnector
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffectConnections.GetOutputConnector
---

# IMILBitmapEffectConnections::GetOutputConnector


## -description

Retrieves the output connector associated with the given pin index.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which output pin to use to retrieve the output connector.

### -param ppConnector [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectoutputconnector">IMILBitmapEffectOutputConnector</a>**</b>

When this method returns, contains the output connector for the given output pin.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.