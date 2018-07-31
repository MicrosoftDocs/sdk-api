---
UID: NF:textserv.ITextHost.TxSetTimer
title: ITextHost::TxSetTimer
author: windows-sdk-content
description: Requests the text host to create a timer with a specified time-out.
old-location: controls\ITextHost_TxSetTimer.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsettimer.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetTimer method, ITextHost.TxSetTimer, ITextHost::TxSetTimer, TxSetTimer, TxSetTimer method [Windows Controls], TxSetTimer method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetTimer, _win32_ITextHost_TxSetTimer_cpp, controls.ITextHost_TxSetTimer, controls._win32_ITextHost_TxSetTimer, textserv/ITextHost::TxSetTimer
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
 - ITextHost.TxSetTimer
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxSetTimer


## -description


Requests the text host to create a timer with a specified time-out.


## -parameters




### -param idTimer [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Timer identifier. 


### -param uTimeout [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Time-out in milliseconds. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Return <b>TRUE</b> if the method succeeds. 

Return <b>FALSE</b> if the method fails. 




## -remarks



<i>idTimer</i> is used in <a href="https://msdn.microsoft.com/eb3f01eb-1b95-49d7-9417-a29fb58d6805">ITextHost::TxKillTimer</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/eb3f01eb-1b95-49d7-9417-a29fb58d6805">TxKillTimer</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

