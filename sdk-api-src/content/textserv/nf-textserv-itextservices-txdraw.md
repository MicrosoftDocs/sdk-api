---
UID: NF:textserv.ITextServices.TxDraw
title: ITextServices::TxDraw (textserv.h)
description: Draws the text services object.
helpviewer_keywords: ["DVASPECT_CONTENT","DVASPECT_DOCPRINT","ITextServices interface [Windows Controls]","TxDraw method","ITextServices.TxDraw","ITextServices::TxDraw","TXTVIEW_ACTIVE","TXTVIEW_INACTIVE","TxDraw","TxDraw method [Windows Controls]","TxDraw method [Windows Controls]","ITextServices interface","_win32_ITextServices_TxDraw","_win32_ITextServices_TxDraw_cpp","controls.ITextServices_TxDraw","controls._win32_ITextServices_TxDraw","textserv/ITextServices::TxDraw"]
old-location: controls\ITextServices_TxDraw.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itextservices\itextservicestxdraw.htm
ms.date: 12/05/2018
ms.keywords: DVASPECT_CONTENT, DVASPECT_DOCPRINT, ITextServices interface [Windows Controls],TxDraw method, ITextServices.TxDraw, ITextServices::TxDraw, TXTVIEW_ACTIVE, TXTVIEW_INACTIVE, TxDraw, TxDraw method [Windows Controls], TxDraw method [Windows Controls],ITextServices interface, _win32_ITextServices_TxDraw, _win32_ITextServices_TxDraw_cpp, controls.ITextServices_TxDraw, controls._win32_ITextServices_TxDraw, textserv/ITextServices::TxDraw
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextServices::TxDraw
 - textserv/ITextServices::TxDraw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextServices.TxDraw
---

# ITextServices::TxDraw


## -description

Draws the text services object.

## -parameters

### -param dwDrawAspect [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Not supported.

### -param pvAspect [in]

Type: <b>void*</b>

Information for drawing optimizations.

### -param ptd [in]

Type: <b><a href="/windows/desktop/api/objidl/ns-objidl-dvtargetdevice">DVTARGETDEVICE</a>*</b>

The target device.

### -param hdcDraw [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

Rendering device context.

### -param hicTargetDev [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Parameter to pass to continue function.

### -param lViewId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The return value is typically <b>S_OK</b>.

## -remarks

This method renders the text services object. It accepts the same parameters as the corresponding <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> method in OLE, with the extra <i>lprcUpdate</i> and the <i>lViewId</i> parameters. It can be used while the host is in-place active or inactive.

The <i>lprcBounds</i> parameter gives the rectangle to render, also called the client rectangle. This rectangle represents the position and extent of the entire image of the text services object to be drawn. It is expressed in the logical coordinate system of <i>hdcDraw</i>. If <i>lprcBounds</i> is <b>NULL</b> then the control must be active. In this case, the text services object should render the in-place active view (that is, the client rectangle that can be obtained by calling <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txgetclientrect">TxGetClientRect</a> on the host).

If the <i>lprcUpdate</i> parameter is not <b>NULL</b>, it gives the rectangle to update inside that client rectangle, in the logical coordinate system of <i>hdcDraw</i>. If <i>lprcUpdate</i> is <b>NULL</b>, the entire client rectangle should be painted.

The text services object should render with the appropriate zoom factor, which can be obtained from the client rectangle and the native size given by <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txgetextent">TxGetExtent</a>. For a discussion of the zoom factor, see <b>TxGetExtent</b>. 

General comments on OLE hosts and <b>ITextServices::TxDraw</b> (also for <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxsetcursor">ITextServices::OnTxSetCursor</a>, and <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-txqueryhitpoint">ITextServices::TxQueryHitPoint</a>):

An OLE host can call the <b>ITextServices::TxDraw</b> method at any time with any rendering device context or client rectangle. An OLE object that is inactive only retains an extent. To get the rectangle in which to render, the host calls the <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> method. This rectangle is valid only for the scope of that method. Thus, the same control can be rendered consecutively in different rectangles and different device contexts, for example, because it is displayed simultaneously in different views on the screen.

Normally, the client rectangle and device context passed to <b>ITextServices::TxDraw</b> should not be cached, because this would force the text services object to recalculate lines for every draw, which would impede performance. Instead, the text services object could cache the information that is computed for a specific client rectangle and device context (such as line breaks). On the next call to <b>ITextServices::TxDraw</b>, however, the validity of the cached information should be checked before it gets used, and updated information should be regenerated, if necessary.

Also, take great care when the control is in-place active. This problem is even more complex since <b>ITextServices::TxDraw</b> can still be called to render other views than the one that is in-place active. In other words, the client rectangle passed to <b>ITextServices::TxDraw</b> may not be the same as the active one (passed to <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxinplaceactivate">ITextServices::OnTxInPlaceActivate</a> and obtained through <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txgetclientrect">TxGetClientRect</a> on the host).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/objidl/ns-objidl-dvtargetdevice">DVTARGETDEVICE</a>



<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxinplaceactivate">OnTxInPlaceActivate</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/win32/api/windef/ns-windef-rectl">RECTL</a>



<b>Reference</b>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txgetclientrect">TxGetClientRect</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txgetextent">TxGetExtent</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>