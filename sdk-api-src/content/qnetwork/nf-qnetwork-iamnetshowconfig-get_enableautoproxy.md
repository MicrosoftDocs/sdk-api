---
UID: NF:qnetwork.IAMNetShowConfig.get_EnableAutoProxy
title: IAMNetShowConfig::get_EnableAutoProxy
author: windows-driver-content
description: The get_EnableAutoProxy method queries whether the control or filter should use the browser's proxy settings.
old-location: dshow\iamnetshowconfig_get_enableautoproxy.htm
old-project: DirectShow
ms.assetid: 7037f326-3320-4e4a-8f6f-feda1a306c2d
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],get_EnableAutoProxy method, IAMNetShowConfig.get_EnableAutoProxy, IAMNetShowConfig::get_EnableAutoProxy, IAMNetShowConfigget_EnableAutoProxy, dshow.iamnetshowconfig_get_enableautoproxy, get_EnableAutoProxy, get_EnableAutoProxy method [DirectShow], get_EnableAutoProxy method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_EnableAutoProxy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Qnetwork.h
api_name:
-	IAMNetShowConfig.get_EnableAutoProxy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IAMNetShowConfig::get_EnableAutoProxy


## -description



The <code>get_EnableAutoProxy</code> method queries whether the control or filter should use the browser's proxy settings.




## -parameters




### -param pEnableAutoProxy

Pointer to a variable that receives a Boolean value.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This flag is <b>TRUE</b> by default.




## -see-also




<a href="https://msdn.microsoft.com/611b43dc-7f6d-404e-90a4-b109b9475fb6">IAMNetShowConfig Interface</a>
 

 

