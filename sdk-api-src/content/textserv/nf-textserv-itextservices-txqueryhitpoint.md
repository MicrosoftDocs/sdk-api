---
UID: NF:textserv.ITextServices.TxQueryHitPoint
title: ITextServices::TxQueryHitPoint
author: windows-sdk-content
description: Tests whether a specified point is within the rectangle of the text services object.
old-location: controls\ITextServices_TxQueryHitPoint.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txqueryhitpoint.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DVASPECT_CONTENT, DVASPECT_DOCPRINT, ITextServices interface [Windows Controls],TxQueryHitPoint method, ITextServices.TxQueryHitPoint, ITextServices::TxQueryHitPoint, TXTHITRESULT_CLOSE, TXTHITRESULT_HIT, TXTHITRESULT_NOHIT, TXTHITRESULT_TRANSPARENT, TxQueryHitPoint, TxQueryHitPoint method [Windows Controls], TxQueryHitPoint method [Windows Controls],ITextServices interface, _win32_ITextServices_TxQueryHitPoint, _win32_ITextServices_TxQueryHitPoint_cpp, controls.ITextServices_TxQueryHitPoint, controls._win32_ITextServices_TxQueryHitPoint, textserv/ITextServices::TxQueryHitPoint
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
 - ITextServices.TxQueryHitPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextServices::TxQueryHitPoint


## -description


Tests whether a specified point is within the rectangle of the text services object.


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
Renders a screen image of the text content to the <i>hdcDraw</i> device context.

The <i>hicTargetDev</i> and <i>ptd</i> parameters give information on the target device context if any (usually a printer).

</td>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_DOCPRINT"></a><a id="dvaspect_docprint"></a><dl>
<dt><b>DVASPECT_DOCPRINT</b></dt>
</dl>
</td>
<td width="60%">
Renders the object to the <i>hdcDraw</i> device context as though it were printed to a printer. Thus, the text services object can optimize for the printer (for example, not painting the background color, if white). Also, certain screen-specific elements (such as the selection) should not be rendered.


<a href="https://msdn.microsoft.com/66798915-af6f-4a18-813b-872bf0298824">ITextServices::TxGetNaturalSize</a> should render the <i>lprcClient</i> rectangle, starting at the current scrolling position.

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

Information on the target device. 


### -param hdcDraw [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

Rendering device context. 


### -param hicTargetDev [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

Target information context. 


### -param lprcClient [in]

Type: <b>LPCRECT</b>

The control's client rectangle, in client (device) coordinates of the view in which the hit testing is done. 


### -param x [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

x-coordinate to check, in client coordinates, of the view in which hit testing is done. 


### -param y [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

y-coordinate to check, in client coordinates, of the view in which hit testing is done. 


### -param pHitResult [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The result of the hit test. It can be any of the following <b>TXTHITRESULT</b> enumeration values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXTHITRESULT_CLOSE"></a><a id="txthitresult_close"></a><dl>
<dt><b>TXTHITRESULT_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
The point is in the client rectangle and close to a nontransparent area.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTHITRESULT_HIT"></a><a id="txthitresult_hit"></a><dl>
<dt><b>TXTHITRESULT_HIT</b></dt>
</dl>
</td>
<td width="60%">
The point is in the client rectangle and either over text or the background is not transparent.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTHITRESULT_NOHIT"></a><a id="txthitresult_nohit"></a><dl>
<dt><b>TXTHITRESULT_NOHIT</b></dt>
</dl>
</td>
<td width="60%">
The point is outside of the client rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTHITRESULT_TRANSPARENT"></a><a id="txthitresult_transparent"></a><dl>
<dt><b>TXTHITRESULT_TRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">
The point is in the client rectangle and either not over text or the background was transparent.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

The return value is an <b>HRESULT</b> code.




## -remarks



This method allows the host to implement transparent hit testing on text.

For more information, see the Remarks section in <a href="https://msdn.microsoft.com/5fb14a41-2e73-4760-ba77-f1bfd2a1184b">ITextServices::TxDraw</a> and <a href="https://msdn.microsoft.com/9656a2ed-bd66-4083-a2b4-c6255f136f9d">ITextServices::OnTxSetCursor</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<a href="https://msdn.microsoft.com/9656a2ed-bd66-4083-a2b4-c6255f136f9d">OnTxSetCursor</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/5fb14a41-2e73-4760-ba77-f1bfd2a1184b">TxDraw</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

