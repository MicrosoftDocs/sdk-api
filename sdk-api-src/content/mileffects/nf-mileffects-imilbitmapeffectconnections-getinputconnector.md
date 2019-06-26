---
UID: NF:mileffects.IMILBitmapEffectConnections.GetInputConnector
title: IMILBitmapEffectConnections::GetInputConnector (mileffects.h)
author: windows-sdk-content
description: Retrieves the input connector associated with the given pin index.
old-location: wibe\_wibe_imilbitmapeffectconnections_getinputconnector.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnections\getinputconnector.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetInputConnector, GetInputConnector method [WPF Bitmap Effects], GetInputConnector method [WPF Bitmap Effects],IMILBitmapEffectConnections interface, IMILBitmapEffectConnections interface [WPF Bitmap Effects],GetInputConnector method, IMILBitmapEffectConnections.GetInputConnector, IMILBitmapEffectConnections::GetInputConnector, _wibe_imilbitmapeffectconnections_getinputconnector, mileffects/IMILBitmapEffectConnections::GetInputConnector, wibe._wibe_imilbitmapeffectconnections_getinputconnector
ms.topic: method
f1_keywords: 
 - "mileffects/IMILBitmapEffectConnections.GetInputConnector"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffectConnections.GetInputConnector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectConnections::GetInputConnector


## -description


Retrieves the input connector associated with the given pin index.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which input pin to use to retrieve the input connector.


### -param ppConnector [out, retval]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectinputconnector">IMILBitmapEffectInputConnector</a>**</b>

When this method returns, contains the input connector for the given input pin.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



