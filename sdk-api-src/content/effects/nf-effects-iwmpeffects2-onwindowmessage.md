---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
 

 

