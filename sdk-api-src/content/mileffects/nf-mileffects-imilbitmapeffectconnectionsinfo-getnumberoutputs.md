---
UID: NF:mileffects.IMILBitmapEffectConnectionsInfo.GetNumberOutputs
title: IMILBitmapEffectConnectionsInfo::GetNumberOutputs
author: windows-driver-content
description: Retrieves the number of output pins the bitmap effect implements.
old-location: wibe\_wibe_imilbitmapeffectconnectionsinfo_getnumberoutputs.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectionsinfo\getnumberoutputs.htm
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: GetNumberOutputs, GetNumberOutputs method [WPF Bitmap Effects], GetNumberOutputs method [WPF Bitmap Effects],IMILBitmapEffectConnectionsInfo interface, IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects],GetNumberOutputs method, IMILBitmapEffectConnectionsInfo.GetNumberOutputs, IMILBitmapEffectConnectionsInfo::GetNumberOutputs, _wibe_imilbitmapeffectconnectionsinfo_getnumberoutputs, mileffects/IMILBitmapEffectConnectionsInfo::GetNumberOutputs, wibe._wibe_imilbitmapeffectconnectionsinfo_getnumberoutputs
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.h
api_name:
-	IMILBitmapEffectConnectionsInfo.GetNumberOutputs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectConnectionsInfo::GetNumberOutputs


## -description


Retrieves the number of output pins the bitmap effect implements.


## -parameters




### -param puiNumOutputs [out, retval]

Type: <b>ULONG*</b>

When this method returns, contains the number of output pins the bitmap effect implements.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



