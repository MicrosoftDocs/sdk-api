---
UID: NF:textserv.ITextServices.TxDraw
title: ITextServices::TxDraw
author: windows-sdk-content
description: Draws the text services object.
old-location: controls\ITextServices_TxDraw.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itextservices\itextservicestxdraw.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DVASPECT_CONTENT, DVASPECT_DOCPRINT, ITextServices interface [Windows Controls],TxDraw method, ITextServices.TxDraw, ITextServices::TxDraw, TXTVIEW_ACTIVE, TXTVIEW_INACTIVE, TxDraw, TxDraw method [Windows Controls], TxDraw method [Windows Controls],ITextServices interface, _win32_ITextServices_TxDraw, _win32_ITextServices_TxDraw_cpp, controls.ITextServices_TxDraw, controls._win32_ITextServices_TxDraw, textserv/ITextServices::TxDraw
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
 - ITextServices.TxDraw
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextServices::TxDraw


## -description


Draws the text services object.


## -parameters




### -param dwDrawAspect [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the aspect to be drawn, that is, how the object is to be represented. Draw aspect can be one of the following values. 

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

<b>ITextServices::TxDraw</b> should render the <i>lprcBounds</i> rectangle, starting at the current scrolling position.

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


### -param lprcBounds [in]

Type: <b>LPCRECTL</b>

The bounding (client) rectangle. 


### -param lprcWBounds [in]

Type: <b>LPCRECTL</b>

The clipping rectangle for metafiles. 


### -param lprcUpdate [in]

Type: <b>LPRECT</b>

The update region inside <i>lprcBounds</i>. 


### -param pfnContinue

Type: <b>BOOL CALLBACK*</b>

Not supported.


### -param dwContinue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Parameter to pass to continue function. 


### -param lViewId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Specifies the view to draw.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXTVIEW_ACTIVE"></a><a id="txtview_active"></a><dl>
<dt><b>TXTVIEW_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Draw the inplace   active view.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTVIEW_INACTIVE"></a><a id="txtview_inactive"></a><dl>
<dt><b>TXTVIEW_INACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Draw a view other than the inplace active view; for example, a print    preview. 

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

The return value is typically <b>S_OK</b>.




## -remarks



This method renders the text services object. It accepts the same parameters as the corresponding <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a> method in OLE, with the extra <i>lprcUpdate</i> and the <i>lViewId</i> parameters. It can be used while the host is in-place active or inactive.

The <i>lprcBounds</i> parameter gives the rectangle to render, also called the client rectangle. This rectangle represents the position and extent of the entire image of the text services object to be drawn. It is expressed in the logical coordinate system of <i>hdcDraw</i>. If <i>lprcBounds</i> is <b>NULL</b> then the control must be active. In this case, the text services object should render the in-place active view (that is, the client rectangle that can be obtained by calling <a href="https://msdn.microsoft.com/library/Bb787656(v=VS.85).aspx">TxGetClientRect</a> on the host).

If the <i>lprcUpdate</i> parameter is not <b>NULL</b>, it gives the rectangle to update inside that client rectangle, in the logical coordinate system of <i>hdcDraw</i>. If <i>lprcUpdate</i> is <b>NULL</b>, the entire client rectangle should be painted.

The text services object should render with the appropriate zoom factor, which can be obtained from the client rectangle and the native size given by <a href="https://msdn.microsoft.com/library/Bb787664(v=VS.85).aspx">TxGetExtent</a>. For a discussion of the zoom factor, see <b>TxGetExtent</b>. 

General comments on OLE hosts and <b>ITextServices::TxDraw</b> (also for <a href="https://msdn.microsoft.com/library/Bb787630(v=VS.85).aspx">ITextServices::OnTxSetCursor</a>, and <a href="https://msdn.microsoft.com/library/Bb787679(v=VS.85).aspx">ITextServices::TxQueryHitPoint</a>):

An OLE host can call the <b>ITextServices::TxDraw</b> method at any time with any rendering device context or client rectangle. An OLE object that is inactive only retains an extent. To get the rectangle in which to render, the host calls the <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a> method. This rectangle is valid only for the scope of that method. Thus, the same control can be rendered consecutively in different rectangles and different device contexts, for example, because it is displayed simultaneously in different views on the screen.

Normally, the client rectangle and device context passed to <b>ITextServices::TxDraw</b> should not be cached, because this would force the text services object to recalculate lines for every draw, which would impede performance. Instead, the text services object could cache the information that is computed for a specific client rectangle and device context (such as line breaks). On the next call to <b>ITextServices::TxDraw</b>, however, the validity of the cached information should be checked before it gets used, and updated information should be regenerated, if necessary.

Also, take great care when the control is in-place active. This problem is even more complex since <b>ITextServices::TxDraw</b> can still be called to render other views than the one that is in-place active. In other words, the client rectangle passed to <b>ITextServices::TxDraw</b> may not be the same as the active one (passed to <a href="https://msdn.microsoft.com/library/Bb787621(v=VS.85).aspx">ITextServices::OnTxInPlaceActivate</a> and obtained through <a href="https://msdn.microsoft.com/library/Bb787656(v=VS.85).aspx">TxGetClientRect</a> on the host). 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/724ff714-c170-4d06-92cb-e042e41c0af2">DVTARGETDEVICE</a>



<a href="https://msdn.microsoft.com/library/Bb787617(v=VS.85).aspx">ITextServices</a>



<a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a>



<a href="https://msdn.microsoft.com/library/Bb787621(v=VS.85).aspx">OnTxInPlaceActivate</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb787656(v=VS.85).aspx">TxGetClientRect</a>



<a href="https://msdn.microsoft.com/library/Bb787664(v=VS.85).aspx">TxGetExtent</a>



<a href="https://msdn.microsoft.com/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls</a>
 

 

