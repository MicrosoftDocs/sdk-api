---
UID: NF:mileffects.IMILBitmapEffectOutputConnector.GetConnection
title: IMILBitmapEffectOutputConnector::GetConnection
author: windows-sdk-content
description: Gets the IMILBitmapEffectInputConnector associated with the output connector.
old-location: wibe\_wibe_imilbitmapeffectoutputconnector_getconnection.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectoutputconnector\getconnection.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: GetConnection, GetConnection method [WPF Bitmap Effects], GetConnection method [WPF Bitmap Effects],IMILBitmapEffectOutputConnector interface, IMILBitmapEffectOutputConnector interface [WPF Bitmap Effects],GetConnection method, IMILBitmapEffectOutputConnector.GetConnection, IMILBitmapEffectOutputConnector::GetConnection, _wibe_imilbitmapeffectoutputconnector_getconnection, mileffects/IMILBitmapEffectOutputConnector::GetConnection, wibe._wibe_imilbitmapeffectoutputconnector_getconnection
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
 - Mileffects.dll
api_name:
 - IMILBitmapEffectOutputConnector.GetConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectOutputConnector::GetConnection


## -description


Gets the <a href="https://msdn.microsoft.com/library/ms735274(v=VS.85).aspx">IMILBitmapEffectInputConnector</a> associated with the output connector.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the desired input connector.


### -param ppConnection [out, retval]

Type: <b><a href="https://msdn.microsoft.com/library/ms735274(v=VS.85).aspx">IMILBitmapEffectInputConnector</a>**</b>

A pointer that receives a pointer to the associated input connector.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



