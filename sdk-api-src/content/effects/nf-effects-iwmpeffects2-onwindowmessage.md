---
UID: NF:effects.IWMPEffects2.OnWindowMessage
title: IWMPEffects2::OnWindowMessage
author: windows-sdk-content
description: The OnWindowMessage method is called by Windows Media Player to pass window messages to a visualization.
old-location: wmp\iwmpeffects2_onwindowmessage.htm
old-project: WMP
ms.assetid: c4efdac9-b50f-4448-98f2-efe015527a4e
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPEffects2 interface [Windows Media Player],OnWindowMessage method, IWMPEffects2.OnWindowMessage, IWMPEffects2::OnWindowMessage, IWMPEffectsOnWindowMessage, OnWindowMessage, OnWindowMessage method [Windows Media Player], OnWindowMessage method [Windows Media Player],IWMPEffects2 interface, effects/IWMPEffects2::OnWindowMessage, wmp.iwmpeffects2_onwindowmessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: effects.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	effects.h
api_name:
-	IWMPEffects2.OnWindowMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IWMPEffects2::OnWindowMessage


## -description



The <b>OnWindowMessage</b> method is called by Windows Media Player to pass window messages to a visualization.




## -parameters




### -param msg [in]

<b>UINT</b> that identifies the window message.


### -param WParam [in]

<b>WPARAM</b> specifying a window message parameter.


### -param LParam [in]

<b>LPARAM</b> specifying a window message parameter.


### -param plResultParam [in]

Pointer to an <b>LRESULT</b> specifying the result code for the window message.


## -returns



This method returns an <b>HRESULT</b>.




## -remarks



Your implementation must only return S_OK if it has handled the window message. If it has not handled the window message, it should return S_FALSE. If this method is not implemented, return E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/44e044c1-97fd-43cb-9530-4556e485f5ae">IWMPEffects2 Interface</a>
 

 

