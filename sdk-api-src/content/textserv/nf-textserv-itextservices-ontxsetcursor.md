---
UID: NF:textserv.ITextServices.OnTxSetCursor
title: ITextServices::OnTxSetCursor
author: windows-sdk-content
description: Notifies the text services object to set the cursor.
old-location: controls\ITextServices_OnTxSetCursor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxsetcursor.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DVASPECT_CONTENT, DVASPECT_DOCPRINT, ITextServices interface [Windows Controls],OnTxSetCursor method, ITextServices.OnTxSetCursor, ITextServices::OnTxSetCursor, OnTxSetCursor, OnTxSetCursor method [Windows Controls], OnTxSetCursor method [Windows Controls],ITextServices interface, _win32_ITextServices_OnTxSetCursor, _win32_ITextServices_OnTxSetCursor_cpp, controls.ITextServices_OnTxSetCursor, controls._win32_ITextServices_OnTxSetCursor, textserv/ITextServices::OnTxSetCursor
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
 - ITextServices.OnTxSetCursor
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextServices::OnTxSetCursor


## -description


Notifies the text services object to set the cursor.


## -parameters




### -param dwDrawAspect [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Draw aspect can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_CONTENT"></a><a id="dvaspect_content"></a><dl>
<dt><b>DVASPECT_CONTENT</b></dt>
</dl>
</td>
<td width="60%">
Renders a screen image of the text content to the <i>hdcDraw</i> device context. The <i>hicTargetDev</i> and <i>ptd</i> parameters give information on the target device context if any (usually a printer).

</td>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_DOCPRINT"></a><a id="dvaspect_docprint"></a><dl>
<dt><b>DVASPECT_DOCPRINT</b></dt>
</dl>
</td>
<td width="60%">
Renders the object to the <i>hdcDraw</i> device context as though it were printed to a printer. Thus, the text services object can optimize for the printer (for example, not painting the background color, if white). Also, certain screen-specific elements (such as the selection) should not be rendered.

<b>ITextServices::OnTxSetCursor</b> should render the <i>lprcClient</i> rectangle, starting at the current scrolling position.

</td>
</tr>
</table>
 


### -param lindex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Not supported.


### -param pvAspect [in]

Type: <b>void*</b>

Information for drawing optimizations. 


### -param ptd [in]

Type: <b><a href="https://msdn.microsoft.com/724ff714-c170-4d06-92cb-e042e41c0af2">DVTARGETDEVICE</a>*</b>

The target device.


### -param hdcDraw [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

Rendering device context. 


### -param hicTargetDev [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

Target information context. 


### -param lprcClient [in]

Type: <b>LPCRECT</b>

The control's client rectangle. The coordinates of the rectangle are in client coordinates of the containing window. <b>NULL</b> is a legal value. 


### -param x [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

x position of cursor, in the client coordinates of the containing window. 


### -param y [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

y position of cursor, in the client coordinates of the containing window. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, the return value is <b>S_OK</b>.

If the method fails, the return value is the following <b>HRESULT</b> code. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more illegal parameters.

</td>
</tr>
</table>
 




## -remarks



The text services object may remeasure as a result of this call to determine the correct cursor. The correct cursor is set through <a href="https://msdn.microsoft.com/ab5b868e-816c-4122-99d2-4351f7ce3613">TxSetCursor</a>.

The <i>lprcClient</i> parameter is the client rectangle of the view of the control over which the mouse cursor is positioned. The <i>lprcClient</i> parameter is in device coordinates of the containing window in the same way the <a href="https://msdn.microsoft.com/e3e14dcd-9236-48bd-a692-6985d8146f81">WM_SIZE</a> message is. This may not be the view that was rendered last. Furthermore, if the control is in-place active, this may not be the current active view . As a consequence, the text services object should check this rectangle against its current cache's value and determine whether recalculating the lines is necessary or not. The zoom factor should be included in this computation. For a discussion of the zoom factor, see <a href="https://msdn.microsoft.com/03cf4acc-f70e-40a4-9050-6e6777867b2b">TxGetExtent</a>.

This method should be called only for screen views of the control. Therefore the device context (DC) is not passed in, but should be assumed to be a screen DC.

For more information, see the Remarks in <a href="https://msdn.microsoft.com/5fb14a41-2e73-4760-ba77-f1bfd2a1184b">ITextServices::TxDraw</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/5fb14a41-2e73-4760-ba77-f1bfd2a1184b">TxDraw</a>



<a href="https://msdn.microsoft.com/03cf4acc-f70e-40a4-9050-6e6777867b2b">TxGetExtent</a>



<a href="https://msdn.microsoft.com/ab5b868e-816c-4122-99d2-4351f7ce3613">TxSetCursor</a>



<a href="https://msdn.microsoft.com/e3e14dcd-9236-48bd-a692-6985d8146f81">WM_SIZE</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

