---
UID: NF:wmprealestate.IWMPWindowMessageSink.OnWindowMessage
title: IWMPWindowMessageSink::OnWindowMessage
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpwindowmessagesink_onwindowmessage.htm
old-project: WMP
ms.assetid: d32caaba-5264-447f-9890-30e2200e28ff
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IWMPWindowMessageSink interface [Windows Media Player],OnWindowMessage method, IWMPWindowMessageSink.OnWindowMessage, IWMPWindowMessageSink::OnWindowMessage, IWMPWindowMessageSinkOnWindowMessageRendering, OnWindowMessage, OnWindowMessage method [Windows Media Player], OnWindowMessage method [Windows Media Player],IWMPWindowMessageSink interface, wmp.iwmpwindowmessagesink_onwindowmessage, wmprealestate/IWMPWindowMessageSink::OnWindowMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmprealestate.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmprealestate.h
api_name:
-	IWMPWindowMessageSink.OnWindowMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPWindowMessageSink::OnWindowMessage


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>OnWindowMessage</b> method receives window messages.


## -parameters




### -param uMsg [in]

The Windows message received.


### -param wparam [in]

Message-specific data.


### -param lparam [in]

Message-specific data.


### -param plRet [out]

Pointer to a long integer containing the return value.


### -param pfHandled [out]

Pointer to a <b>Boolean</b>, true indicating handled.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



When a rendering plug-in window is not hosted in the Windows Media Player UI, such as when the Player is in windowless mode or the Player is rendering Windows Media video, it needs a mechanism to receive window messages from the Player. In these cases, the Player forwards window messages to the plug-in by calling this method.

Windows Media Player queries all active rendering plug-ins to determine whether they support this method and automatically forwards window messages to each plug-in that does.




## -see-also




<a href="https://msdn.microsoft.com/b601816f-17eb-4195-9c2e-5adcf2c8663e">IWMPWindowMessageSink Interface (deprecated)</a>
 

 

