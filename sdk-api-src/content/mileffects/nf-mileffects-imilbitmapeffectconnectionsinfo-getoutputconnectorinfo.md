---
UID: NF:mileffects.IMILBitmapEffectConnectionsInfo.GetOutputConnectorInfo
title: IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo (mileffects.h)
description: Retrieves the IMILBitmapEffectConnectorInfo associated with the given output pin.
helpviewer_keywords: ["GetOutputConnectorInfo","GetOutputConnectorInfo method [WPF Bitmap Effects]","GetOutputConnectorInfo method [WPF Bitmap Effects]","IMILBitmapEffectConnectionsInfo interface","IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects]","GetOutputConnectorInfo method","IMILBitmapEffectConnectionsInfo.GetOutputConnectorInfo","IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo","_wibe_imilbitmapeffectconnectionsinfo_getoutputconnectorinfo","mileffects/IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo","wibe._wibe_imilbitmapeffectconnectionsinfo_getoutputconnectorinfo"]
old-location: wibe\_wibe_imilbitmapeffectconnectionsinfo_getoutputconnectorinfo.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectionsinfo\getoutputconnectorinfo.htm
ms.date: 12/05/2018
ms.keywords: GetOutputConnectorInfo, GetOutputConnectorInfo method [WPF Bitmap Effects], GetOutputConnectorInfo method [WPF Bitmap Effects],IMILBitmapEffectConnectionsInfo interface, IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects],GetOutputConnectorInfo method, IMILBitmapEffectConnectionsInfo.GetOutputConnectorInfo, IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo, _wibe_imilbitmapeffectconnectionsinfo_getoutputconnectorinfo, mileffects/IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo, wibe._wibe_imilbitmapeffectconnectionsinfo_getoutputconnectorinfo
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
 - IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo
 - mileffects/IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo
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
 - IMILBitmapEffectConnectionsInfo.GetOutputConnectorInfo
---

# IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo


## -description

Retrieves the <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnectorinfo">IMILBitmapEffectConnectorInfo</a> associated with the given output pin.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which output pin to query for connector information.

### -param ppConnectorInfo [out]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnectorinfo">IMILBitmapEffectConnectorInfo</a>**</b>

When this method returns, contain the connector information for the given output pin.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.