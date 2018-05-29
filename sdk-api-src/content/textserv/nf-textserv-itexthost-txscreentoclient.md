---
UID: NF:textserv.ITextHost.TxScreenToClient
title: ITextHost::TxScreenToClient
author: windows-sdk-content
description: Converts the screen coordinates to the text host window coordinates.
old-location: controls\ITextHost_TxScreenToClient.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxscreentoclient.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ITextHost interface [Windows Controls],TxScreenToClient method, ITextHost.TxScreenToClient, ITextHost::TxScreenToClient, TxScreenToClient, TxScreenToClient method [Windows Controls], TxScreenToClient method [Windows Controls],ITextHost interface, _win32_ITextHost_TxScreenToClient, _win32_ITextHost_TxScreenToClient_cpp, controls.ITextHost_TxScreenToClient, controls._win32_ITextHost_TxScreenToClient, textserv/ITextHost::TxScreenToClient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	ITextHost.TxScreenToClient
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxScreenToClient


## -description


Converts the screen coordinates to the text host window coordinates.


## -parameters




### -param lppt [in]

Type: <b>LPPOINT</b>

The screen coordinates to convert. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Return <b>TRUE</b> if the call succeeds. 

Return <b>FALSE</b> if the call fails. 




## -see-also




<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls Overview</a>
 

 

