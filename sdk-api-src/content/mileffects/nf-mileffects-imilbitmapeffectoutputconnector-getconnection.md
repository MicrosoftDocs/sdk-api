---
UID: NF:mileffects.IMILBitmapEffectOutputConnector.GetConnection
title: IMILBitmapEffectOutputConnector::GetConnection (mileffects.h)
description: Gets the IMILBitmapEffectInputConnector associated with the output connector.
helpviewer_keywords: ["GetConnection","GetConnection method [WPF Bitmap Effects]","GetConnection method [WPF Bitmap Effects]","IMILBitmapEffectOutputConnector interface","IMILBitmapEffectOutputConnector interface [WPF Bitmap Effects]","GetConnection method","IMILBitmapEffectOutputConnector.GetConnection","IMILBitmapEffectOutputConnector::GetConnection","_wibe_imilbitmapeffectoutputconnector_getconnection","mileffects/IMILBitmapEffectOutputConnector::GetConnection","wibe._wibe_imilbitmapeffectoutputconnector_getconnection"]
old-location: wibe\_wibe_imilbitmapeffectoutputconnector_getconnection.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectoutputconnector\getconnection.htm
ms.date: 12/05/2018
ms.keywords: GetConnection, GetConnection method [WPF Bitmap Effects], GetConnection method [WPF Bitmap Effects],IMILBitmapEffectOutputConnector interface, IMILBitmapEffectOutputConnector interface [WPF Bitmap Effects],GetConnection method, IMILBitmapEffectOutputConnector.GetConnection, IMILBitmapEffectOutputConnector::GetConnection, _wibe_imilbitmapeffectoutputconnector_getconnection, mileffects/IMILBitmapEffectOutputConnector::GetConnection, wibe._wibe_imilbitmapeffectoutputconnector_getconnection
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
req.dll: Mileffects.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
f1_keywords:
 - IMILBitmapEffectOutputConnector::GetConnection
 - mileffects/IMILBitmapEffectOutputConnector::GetConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectOutputConnector.GetConnection
---

# IMILBitmapEffectOutputConnector::GetConnection


## -description

Gets the <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectinputconnector">IMILBitmapEffectInputConnector</a> associated with the output connector.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the desired input connector.

### -param ppConnection [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectinputconnector">IMILBitmapEffectInputConnector</a>**</b>

A pointer that receives a pointer to the associated input connector.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.