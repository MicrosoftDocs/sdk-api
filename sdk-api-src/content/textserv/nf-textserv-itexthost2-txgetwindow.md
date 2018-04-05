---
UID: NF:textserv.ITextHost2.TxGetWindow
title: ITextHost2::TxGetWindow method
author: windows-driver-content
description: Retrieves the handle of the text host window for the rich edit control.
old-location: controls\itexthost2_txgetwindow.htm
old-project: Controls
ms.assetid: 42594B92-298B-4659-87EC-D10C6996CECF
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: ITextHost2, ITextHost2 interface [Windows Controls], TxGetWindow method, ITextHost2::TxGetWindow, TxGetWindow method [Windows Controls], TxGetWindow method [Windows Controls], ITextHost2 interface, TxGetWindow,ITextHost2.TxGetWindow, controls.itexthost2_txgetwindow, textserv/ITextHost2::TxGetWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextHost2.TxGetWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost2::TxGetWindow method


## -description


Retrieves the handle of the text host window for the rich edit control. 


## -parameters




### -param phwnd

Type: <b>HWND*</b>

The handle of the text host window.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A715E70C-E8BB-4796-BDA6-90B745EC7761">ITextHost2</a>
 

 

