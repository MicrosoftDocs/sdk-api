---
UID: NF:textserv.ITextHost2.TxGetHorzExtent
title: ITextHost2::TxGetHorzExtent
author: windows-driver-content
description: Gets the horizontal scroll extent of the text host window.
old-location: controls\itexthost2_txgethorzextent.htm
old-project: Controls
ms.assetid: 86D53FEF-DB50-41F6-AC99-106FC01BCD61
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxGetHorzExtent method, ITextHost2.TxGetHorzExtent, ITextHost2::TxGetHorzExtent, TxGetHorzExtent, TxGetHorzExtent method [Windows Controls], TxGetHorzExtent method [Windows Controls],ITextHost2 interface, controls.itexthost2_txgethorzextent, textserv/ITextHost2::TxGetHorzExtent
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
-	ITextHost2.TxGetHorzExtent
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost2::TxGetHorzExtent


## -description


Gets the horizontal scroll extent of the text host window.


## -parameters




### -param plHorzExtent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

The horizontal scroll extent.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A rich edit control doesn't use the return value; instead, they get the scroll width from the widest line.




## -see-also




<a href="https://msdn.microsoft.com/A715E70C-E8BB-4796-BDA6-90B745EC7761">ITextHost2</a>
 

 

