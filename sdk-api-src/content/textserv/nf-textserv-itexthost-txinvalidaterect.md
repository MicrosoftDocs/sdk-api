---
UID: NF:textserv.ITextHost.TxInvalidateRect
title: ITextHost::TxInvalidateRect
author: windows-sdk-content
description: Specifies a rectangle for the text host to add to the update region of the text host window.
old-location: controls\ITextHost_TxInvalidateRect.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxinvalidaterect.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextHost interface [Windows Controls],TxInvalidateRect method, ITextHost.TxInvalidateRect, ITextHost::TxInvalidateRect, TxInvalidateRect, TxInvalidateRect method [Windows Controls], TxInvalidateRect method [Windows Controls],ITextHost interface, _win32_ITextHost_TxInvalidateRect, _win32_ITextHost_TxInvalidateRect_cpp, controls.ITextHost_TxInvalidateRect, controls._win32_ITextHost_TxInvalidateRect, textserv/ITextHost::TxInvalidateRect
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
 - ITextHost.TxInvalidateRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost::TxInvalidateRect


## -description


Specifies a rectangle for the text host to add to the update region of the text host window.


## -parameters




### -param prc [in]

Type: <b>LPCRECT</b>

The invalid rectangle. 


### -param fMode [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether the background within the update region is to be erased when the update region is processed. If this parameter is <b>TRUE</b>, the background is erased when the <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function is called. If this parameter is <b>FALSE</b>, the background remains unchanged. 


## -returns



This method has no return value.




## -remarks



This function may be called while inactive; however, the host implementation is free to invalidate an area greater than the requested 
				<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls Overview</a>
 

 

