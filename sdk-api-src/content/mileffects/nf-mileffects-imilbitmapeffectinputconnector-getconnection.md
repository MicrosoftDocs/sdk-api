---
UID: NF:mileffects.IMILBitmapEffectInputConnector.GetConnection
title: IMILBitmapEffectInputConnector::GetConnection
author: windows-sdk-content
description: Gets the IMILBitmapEffectOutputConnector the input connector is connected to.
old-location: wibe\_wibe_imilbitmapeffectinputconnector_getconnection.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectinputconnector\getconnection.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetConnection, GetConnection method [WPF Bitmap Effects], GetConnection method [WPF Bitmap Effects],IMILBitmapEffectInputConnector interface, IMILBitmapEffectInputConnector interface [WPF Bitmap Effects],GetConnection method, IMILBitmapEffectInputConnector.GetConnection, IMILBitmapEffectInputConnector::GetConnection, _wibe_imilbitmapeffectinputconnector_getconnection, mileffects/IMILBitmapEffectInputConnector::GetConnection, wibe._wibe_imilbitmapeffectinputconnector_getconnection
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
req.lib: 
req.dll: Mileffects.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectInputConnector.GetConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
- apiref
: 
- COM
: 
- mileffects.h
: 
- IMILBitmapEffectInputConnector.GetConnection
: 
---

# IMILBitmapEffectInputConnector::GetConnection


## -description


Gets the <a href="https://msdn.microsoft.com/36a2d9da-7a25-4316-acdf-8add4016f18f">IMILBitmapEffectOutputConnector</a> the input connector is connected to.


## -parameters




### -param ppConnector [out, retval]

Type: <b><a href="https://msdn.microsoft.com/36a2d9da-7a25-4316-acdf-8add4016f18f">IMILBitmapEffectOutputConnector</a>**</b>

A pointer that receives a pointer to the associated output connector.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



