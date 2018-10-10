---
UID: NF:textserv.ITextHost.TxScrollWindowEx
title: ITextHost::TxScrollWindowEx
author: windows-sdk-content
description: Requests the text host to scroll the content of the specified client area.
old-location: controls\ITextHost_TxScrollWindowEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxscrollwindowex.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ITextHost interface [Windows Controls],TxScrollWindowEx method, ITextHost.TxScrollWindowEx, ITextHost::TxScrollWindowEx, SW_ERASE, SW_INVALIDATE, SW_SCROLLCHILDREN, SW_SMOOTHSCROLL, TxScrollWindowEx, TxScrollWindowEx method [Windows Controls], TxScrollWindowEx method [Windows Controls],ITextHost interface, _win32_ITextHost_TxScrollWindowEx, _win32_ITextHost_TxScrollWindowEx_cpp, controls.ITextHost_TxScrollWindowEx, controls._win32_ITextHost_TxScrollWindowEx, textserv/ITextHost::TxScrollWindowEx
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
 - ITextHost.TxScrollWindowEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost::TxScrollWindowEx


## -description


Requests the text host to scroll the content of the specified client area.


## -parameters




### -param dx [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Amount of horizontal scrolling. 


### -param dy [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Amount of vertical scrolling. 


### -param lprcScroll [in]

Type: <b>LPCRECT</b>

The coordinates for the scroll rectangle. 


### -param lprcClip [in]

Type: <b>LPCRECT</b>

The coordinates for the clip rectangle. 


### -param hrgnUpdate [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRGN</a></b>

Handle to the update region. 


### -param lprcUpdate [in]

Type: <b>LPRECT</b>

The coordinates for the update rectangle. 


### -param fuScroll [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Scrolling flags. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SW_ERASE"></a><a id="sw_erase"></a><dl>
<dt><b>SW_ERASE</b></dt>
</dl>
</td>
<td width="60%">
Erases the newly invalidated region by sending a 
								<a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8acbe1">WM_ERASEBKGND</a> message to the window when specified with the SW_INVALIDATE flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_INVALIDATE"></a><a id="sw_invalidate"></a><dl>
<dt><b>SW_INVALIDATE</b></dt>
</dl>
</td>
<td width="60%">
Invalidates the region identified by the 
								<i>hrgnUpdate</i> parameter after scrolling.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SCROLLCHILDREN"></a><a id="sw_scrollchildren"></a><dl>
<dt><b>SW_SCROLLCHILDREN</b></dt>
</dl>
</td>
<td width="60%">
Scrolls all child windows that intersect the rectangle pointed to by the 
								<i>lprcScroll</i> parameter. The child windows are scrolled by the number of pixels specified by the 
								<i>dx</i> and 
								<i>dy</i> parameters. The system sends a 
								<a href="https://msdn.microsoft.com/552ddc26-fe63-449b-8c82-bb927a2c1c41">WM_MOVE</a> message to all child windows that intersect the 
								<i>lprcScroll</i> rectangle, even if they do not move.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SMOOTHSCROLL"></a><a id="sw_smoothscroll"></a><dl>
<dt><b>SW_SMOOTHSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Scrolls using smooth scrolling. Use the 
								<a href="https://msdn.microsoft.com/9f79d489-ff3f-437c-821e-fd353d712c7b">HIWORD</a> portion of the 
								<i>fuScroll</i> parameter to indicate how much time the smooth-scrolling operation should take.

</td>
</tr>
</table>
 


## -returns



There is no return value.




## -remarks



This method is only valid when the control is in-place active; calls while the control is inactive may fail.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

