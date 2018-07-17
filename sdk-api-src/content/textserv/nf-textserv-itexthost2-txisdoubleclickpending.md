---
UID: NF:textserv.ITextHost2.TxIsDoubleClickPending
title: ITextHost2::TxIsDoubleClickPending
author: windows-sdk-content
description: Discovers whether the message queue contains a WM_LBUTTONDBLCLK message that is pending for the text host window.
old-location: controls\itexthost2_txisdoubleclickpending.htm
old-project: Controls
ms.assetid: 24051A4F-70CD-4147-B623-BC818F3F9AF2
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxIsDoubleClickPending method, ITextHost2.TxIsDoubleClickPending, ITextHost2::TxIsDoubleClickPending, TxIsDoubleClickPending, TxIsDoubleClickPending method [Windows Controls], TxIsDoubleClickPending method [Windows Controls],ITextHost2 interface, controls.itexthost2_txisdoubleclickpending, textserv/ITextHost2::TxIsDoubleClickPending
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost2.TxIsDoubleClickPending
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost2::TxIsDoubleClickPending


## -description


Discovers whether the message queue contains a <a href="https://msdn.microsoft.com/library/ms645606(v=VS.85).aspx">WM_LBUTTONDBLCLK</a>  message that is pending for the text host window.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if a <a href="https://msdn.microsoft.com/library/ms645606(v=VS.85).aspx">WM_LBUTTONDBLCLK</a> message is pending, or <b>FALSE</b> if not.




## -see-also




<a href="https://msdn.microsoft.com/A715E70C-E8BB-4796-BDA6-90B745EC7761">ITextHost2</a>
 

 

