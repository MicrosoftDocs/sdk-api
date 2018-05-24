---
UID: NF:textserv.ITextHost2.TxShowDropCaret
title: ITextHost2::TxShowDropCaret
author: windows-driver-content
description: Shows or hides the caret during the drop portion of a drag-and-drop operation (Direct2D only).
old-location: controls\itexthost2_txshowdropcaret.htm
old-project: Controls
ms.assetid: D7FAD45E-3467-4F07-A0D9-3131E48C314B
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxShowDropCaret method, ITextHost2.TxShowDropCaret, ITextHost2::TxShowDropCaret, TxShowDropCaret, TxShowDropCaret method [Windows Controls], TxShowDropCaret method [Windows Controls],ITextHost2 interface, controls.itexthost2_txshowdropcaret, textserv/ITextHost2::TxShowDropCaret
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
-	ITextHost2.TxShowDropCaret
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost2::TxShowDropCaret


## -description


Shows or hides the  caret during the drop portion of a drag-and-drop operation (Direct2D only).


## -parameters




### -param fShow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Show or hide flag. <b>TRUE</b> shows the drop caret, and <b>FALSE</b> hides it.


### -param hdc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

The HDC.


### -param prc

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">LPCRECT</a></b>

The drop caret rectangle.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A715E70C-E8BB-4796-BDA6-90B745EC7761">ITextHost2</a>
 

 

