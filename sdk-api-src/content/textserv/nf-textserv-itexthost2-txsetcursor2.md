---
UID: NF:textserv.ITextHost2.TxSetCursor2
title: ITextHost2::TxSetCursor2
author: windows-sdk-content
description: Sets the shape of the cursor in the text host window.
old-location: controls\itexthost2_txsetcursor2.htm
old-project: Controls
ms.assetid: 9671AEEC-CA31-4CE7-8B40-57859E36EF23
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxSetCursor2 method, ITextHost2.TxSetCursor2, ITextHost2::TxSetCursor2, TxSetCursor2, TxSetCursor2 method [Windows Controls], TxSetCursor2 method [Windows Controls],ITextHost2 interface, controls.itexthost2_txsetcursor2, textserv/ITextHost2::TxSetCursor2
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextHost2.TxSetCursor2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost2::TxSetCursor2


## -description


Sets the shape of the cursor in the text host window. 


## -parameters




### -param hcur

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HCURSOR</a></b>

The new cursor shape.


### -param bText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the cursor is used for text, or <b>FALSE</b> if not.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HCURSOR</a></b>

Returns the cursor that <i>hcur</i> is replacing. 




## -see-also




<a href="https://msdn.microsoft.com/A715E70C-E8BB-4796-BDA6-90B745EC7761">ITextHost2</a>



<a href="https://msdn.microsoft.com/ab5b868e-816c-4122-99d2-4351f7ce3613">ITextHost::TxSetCursor</a>



<a href="https://msdn.microsoft.com/9656a2ed-bd66-4083-a2b4-c6255f136f9d">ITextServices::OnTxSetCursor</a>
 

 

