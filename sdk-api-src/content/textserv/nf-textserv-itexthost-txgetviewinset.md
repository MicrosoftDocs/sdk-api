---
UID: NF:textserv.ITextHost.TxGetViewInset
title: ITextHost::TxGetViewInset
author: windows-sdk-content
description: Requests the dimensions of the white space inset around the text in the text host window.
old-location: controls\ITextHost_TxGetViewInset.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxgetviewinset.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetViewInset method, ITextHost.TxGetViewInset, ITextHost::TxGetViewInset, TxGetViewInset, TxGetViewInset method [Windows Controls], TxGetViewInset method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetViewInset, _win32_ITextHost_TxGetViewInset_cpp, controls.ITextHost_TxGetViewInset, controls._win32_ITextHost_TxGetViewInset, textserv/ITextHost::TxGetViewInset
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
 - ITextHost.TxGetViewInset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost::TxGetViewInset


## -description


Requests the dimensions of the white space inset around the text in the text host window.


## -parameters




### -param prc

Type: <b>LPRECT</b>

The inset size, in client coordinates. The top, bottom, left, and right members of the 
					<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure indicate how far in each direction the drawing should be inset. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

The return value is <b>S_OK</b>.




## -remarks



The view inset is the amount of space on each side between the client rectangle and the view rectangle. The view rectangle (also called the Formatting rectangle) is the rectangle in which the text should be formatted .

The view insets are passed in a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure, but this is not really a rectangle. It should be treated as four independent values to subtract on each side of the client rectangle to figure the view rectangle.

The view insets are passed in HIMETRIC (each HIMETRIC unit corresponds to 0.01 millimeter) so that they do not depend on the client rectangle and the rendering device context.

View insets can be negative on either side of the client rectangle, leading to a bigger view rectangle than the client rectangle. The text should then be clipped to the client rectangle. If the view rectangle is wider than the client rectangle, then the host may add a horizontal scroll bar to the control.

Single line–text services objects ignore the right boundary of the view rectangle when formatting text.

The view inset is available from the host at all times, active or inactive.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls Overview</a>
 

 

