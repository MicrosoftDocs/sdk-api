---
UID: NF:wmprealestate.IWMPNodeWindowedHost.OnWindowMessageFromRenderer
title: IWMPNodeWindowedHost::OnWindowMessageFromRenderer method
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnodewindowedhost_onwindowmessagefromrenderer.htm
old-project: WMP
ms.assetid: 44b334af-503d-4a67-88be-9c97910c315a
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPNodeWindowedHost, IWMPNodeWindowedHost interface [Windows Media Player], OnWindowMessageFromRenderer method, IWMPNodeWindowedHost::OnWindowMessageFromRenderer, IWMPNodeWindowedHostOnWindowMessageFromRendererRendering, OnWindowMessageFromRenderer method [Windows Media Player], OnWindowMessageFromRenderer method [Windows Media Player], IWMPNodeWindowedHost interface, OnWindowMessageFromRenderer,IWMPNodeWindowedHost.OnWindowMessageFromRenderer, wmp.iwmpnodewindowedhost_onwindowmessagefromrenderer, wmprealestate/IWMPNodeWindowedHost::OnWindowMessageFromRenderer
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
-	wmp.dll
api_name:
-	IWMPNodeWindowedHost.OnWindowMessageFromRenderer
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeWindowedHost::OnWindowMessageFromRenderer method


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>OnWindowMessageFromRenderer</b> method sends Windows messages from the plug-in to Windows Media Player.


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



You must forward certain messages received by your plug-in window to Windows Media Player if they are not handled by your window code. For instance, keyboard messages and mouse messages might need to be handled by the Player or Internet Explorer. Do not forward messages received from Windows Media Player in <b>IWMPWindowMessageSink::OnWindowMessage</b>.

The following window messages must be forwarded:

<ul>
<li>
            WM_KEYDOWN
          </li>
<li>
            WM_KEYUP
          </li>
<li>
            WM_LBUTTONDBLCLK
          </li>
<li>
            WM_LBUTTONDOWN
          </li>
<li>
            WM_LBUTTONUP
          </li>
<li>
            WM_MBUTTONDBLCLK
          </li>
<li>
            WM_MBUTTONDOWN
          </li>
<li>
            WM_MBUTTONUP
          </li>
<li>
            WM_MOUSEACTIVATE
          </li>
<li>
            WM_MOUSEMOVE
          </li>
<li>
            WM_NCLBUTTONDBLCLK
          </li>
<li>
            WM_NCLBUTTONDOWN
          </li>
<li>
            WM_NCLBUTTONUP
          </li>
<li>
            WM_NCMBUTTONDBLCLK
          </li>
<li>
            WM_NCMBUTTONDOWN
          </li>
<li>
            WM_NCMBUTTONUP
          </li>
<li>
            WM_NCMOUSEMOVE
          </li>
<li>
            WM_NCRBUTTONDBLCLK
          </li>
<li>
            WM_NCRBUTTONDOWN
          </li>
<li>
            WM_NCRBUTTONUP
          </li>
<li>
            WM_RBUTTONDBLCLK
          </li>
<li>
            WM_RBUTTONDOWN
          </li>
<li>
            WM_RBUTTONUP
          </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e350bc92-07cc-414d-8733-ad83c2454a7e">IWMPNodeWindowedHost Interface (deprecated)</a>



<a href="https://msdn.microsoft.com/d32caaba-5264-447f-9890-30e2200e28ff">IWMPWindowMessageSink::OnWindowMessage (deprecated)</a>
 

 

