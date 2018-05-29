---
UID: NF:qnetwork.IAMNetShowConfig.get_EnableTCP
title: IAMNetShowConfig::get_EnableTCP
author: windows-sdk-content
description: The get_EnableTCP method queries whether TCP-based streaming is enabled.
old-location: dshow\iamnetshowconfig_get_enabletcp.htm
old-project: DirectShow
ms.assetid: b4282f84-e05b-407f-9425-0690783957c4
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],get_EnableTCP method, IAMNetShowConfig.get_EnableTCP, IAMNetShowConfig::get_EnableTCP, IAMNetShowConfigget_EnableTCP, dshow.iamnetshowconfig_get_enabletcp, get_EnableTCP, get_EnableTCP method [DirectShow], get_EnableTCP method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_EnableTCP
ms.prod: windows
ms.technology: windows-sdk
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
-	IAMNetShowConfig.get_EnableTCP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAMNetShowConfig::get_EnableTCP


## -description



The <code>get_EnableTCP</code> method queries whether TCP-based streaming is enabled.




## -parameters




### -param pEnableTCP

Pointer to a variable that receives a Boolean value.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/611b43dc-7f6d-404e-90a4-b109b9475fb6">IAMNetShowConfig Interface</a>



<a href="https://msdn.microsoft.com/95c689c9-34f6-49b2-bd3b-0f68a110c4f2">IAMNetShowConfig::get_EnableUDP</a>
 

 

