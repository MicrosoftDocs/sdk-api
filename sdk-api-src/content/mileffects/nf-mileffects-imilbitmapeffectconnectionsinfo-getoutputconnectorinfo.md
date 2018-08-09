---
UID: NF:mileffects.IMILBitmapEffectConnectionsInfo.GetOutputConnectorInfo
title: IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo
author: windows-sdk-content
description: Retrieves the IMILBitmapEffectConnectorInfo associated with the given output pin.
old-location: wibe\_wibe_imilbitmapeffectconnectionsinfo_getoutputconnectorinfo.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectionsinfo\getoutputconnectorinfo.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetOutputConnectorInfo, GetOutputConnectorInfo method [WPF Bitmap Effects], GetOutputConnectorInfo method [WPF Bitmap Effects],IMILBitmapEffectConnectionsInfo interface, IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects],GetOutputConnectorInfo method, IMILBitmapEffectConnectionsInfo.GetOutputConnectorInfo, IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo, _wibe_imilbitmapeffectconnectionsinfo_getoutputconnectorinfo, mileffects/IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo, wibe._wibe_imilbitmapeffectconnectionsinfo_getoutputconnectorinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffectConnectionsInfo.GetOutputConnectorInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo


## -description


Retrieves the <a href="https://msdn.microsoft.com/18f9260d-b7cd-4b45-a7bd-f3bd3647eebe">IMILBitmapEffectConnectorInfo</a> associated with the given output pin.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which output pin to query for connector information.


### -param ppConnectorInfo [out]

Type: <b><a href="https://msdn.microsoft.com/18f9260d-b7cd-4b45-a7bd-f3bd3647eebe">IMILBitmapEffectConnectorInfo</a>**</b>

When this method returns, contain the connector information for the given output pin.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



