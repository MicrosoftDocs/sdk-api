---
UID: NF:mileffects.IMILBitmapEffectConnectionsInfo.GetInputConnectorInfo
title: IMILBitmapEffectConnectionsInfo::GetInputConnectorInfo (mileffects.h)
description: Retrieves the IMILBitmapEffectConnectorInfo associated with the given input pin.
helpviewer_keywords: ["GetInputConnectorInfo","GetInputConnectorInfo method [WPF Bitmap Effects]","GetInputConnectorInfo method [WPF Bitmap Effects]","IMILBitmapEffectConnectionsInfo interface","IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects]","GetInputConnectorInfo method","IMILBitmapEffectConnectionsInfo.GetInputConnectorInfo","IMILBitmapEffectConnectionsInfo::GetInputConnectorInfo","_wibe_imilbitmapeffectconnectionsinfo_getinputconnectorinfo","mileffects/IMILBitmapEffectConnectionsInfo::GetInputConnectorInfo","wibe._wibe_imilbitmapeffectconnectionsinfo_getinputconnectorinfo"]
old-location: wibe\_wibe_imilbitmapeffectconnectionsinfo_getinputconnectorinfo.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectionsinfo\getinputconnectorinfo.htm
ms.date: 12/05/2018
ms.keywords: GetInputConnectorInfo, GetInputConnectorInfo method [WPF Bitmap Effects], GetInputConnectorInfo method [WPF Bitmap Effects],IMILBitmapEffectConnectionsInfo interface, IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects],GetInputConnectorInfo method, IMILBitmapEffectConnectionsInfo.GetInputConnectorInfo, IMILBitmapEffectConnectionsInfo::GetInputConnectorInfo, _wibe_imilbitmapeffectconnectionsinfo_getinputconnectorinfo, mileffects/IMILBitmapEffectConnectionsInfo::GetInputConnectorInfo, wibe._wibe_imilbitmapeffectconnectionsinfo_getinputconnectorinfo
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
 - IMILBitmapEffectConnectionsInfo::GetInputConnectorInfo
 - mileffects/IMILBitmapEffectConnectionsInfo::GetInputConnectorInfo
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
 - IMILBitmapEffectConnectionsInfo.GetInputConnectorInfo
---

# IMILBitmapEffectConnectionsInfo::GetInputConnectorInfo


## -description

Retrieves the <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnectorinfo">IMILBitmapEffectConnectorInfo</a> associated with the given input pin.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which input pin to query for connector information.

### -param ppConnectorInfo [out]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnectorinfo">IMILBitmapEffectConnectorInfo</a>**</b>

When this method returns, contain the connector information for the given input pin.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.