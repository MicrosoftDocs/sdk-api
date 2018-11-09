---
UID: NF:textserv.ITextHost.TxSetScrollRange
title: ITextHost::TxSetScrollRange
author: windows-sdk-content
description: Sets the minimum and maximum position values for the specified scroll bar in the text host window.
old-location: controls\ITextHost_TxSetScrollRange.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsetscrollrange.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetScrollRange method, ITextHost.TxSetScrollRange, ITextHost::TxSetScrollRange, TxSetScrollRange, TxSetScrollRange method [Windows Controls], TxSetScrollRange method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetScrollRange, _win32_ITextHost_TxSetScrollRange_cpp, controls.ITextHost_TxSetScrollRange, controls._win32_ITextHost_TxSetScrollRange, textserv/ITextHost::TxSetScrollRange
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
 - ITextHost.TxSetScrollRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost::TxSetScrollRange


## -description


Sets the minimum and maximum position values for the specified scroll bar in the text host window.


## -parameters




### -param fnBar [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Scroll bar flag. If this is SB_HORZ, horizontal scrolling is done. By default, vertical scrolling is done. 


### -param nMinPos [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Minimum scrolling position. 


### -param nMaxPos [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Maximum scrolling position. 


### -param fRedraw

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Redraw flag. If <b>TRUE</b>, the scroll bar is redrawn to reflect the changes. If <b>FALSE</b>, the scroll bar is not redrawn. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Return <b>TRUE</b> if the arrows are enabled or disabled as specified. 

Return <b>FALSE</b> if the arrows are already in the requested state or an error occurs. 




## -remarks



This method is only valid when the control is in-place active; calls while the control is inactive may fail.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls Overview</a>
 

 

