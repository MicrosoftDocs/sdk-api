---
UID: NF:textserv.ITextHost.TxSetTimer
title: ITextHost::TxSetTimer
author: windows-sdk-content
description: Requests the text host to create a timer with a specified time-out.
old-location: controls\ITextHost_TxSetTimer.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsettimer.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetTimer method, ITextHost.TxSetTimer, ITextHost::TxSetTimer, TxSetTimer, TxSetTimer method [Windows Controls], TxSetTimer method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetTimer, _win32_ITextHost_TxSetTimer_cpp, controls.ITextHost_TxSetTimer, controls._win32_ITextHost_TxSetTimer, textserv/ITextHost::TxSetTimer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
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
req.typenames: 
req.redist: 
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



<i>idTimer</i> is used in <a href="https://msdn.microsoft.com/en-us/library/Bb787708(v=VS.85).aspx">ITextHost::TxKillTimer</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787708(v=VS.85).aspx">TxKillTimer</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls</a>
 

 

