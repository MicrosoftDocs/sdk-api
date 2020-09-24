---
UID: NF:imepad.IImePad.Request
title: IImePad::Request (imepad.h)
description: Called by an IImePadApplet to insert text into an app.
helpviewer_keywords: ["IImePad interface [Internationalization for Windows Applications]","Request method","IImePad.Request","IImePad::Request","IMEPADREQ_CHANGESTRING","IMEPADREQ_DELETESTRING","IMEPADREQ_FORCEIMEPADWINDOWSHOW","IMEPADREQ_GETAPPLETUISTYLE","IMEPADREQ_GETAPPLHWND","IMEPADREQ_GETCOMPOSITIONSTRING","IMEPADREQ_GETCOMPOSITIONSTRINGINFO","IMEPADREQ_GETCONVERSIONSTATUS","IMEPADREQ_GETCURRENTIMEINFO","IMEPADREQ_GETCURRENTUILANG","IMEPADREQ_GETDEFAULTUILANGID","IMEPADREQ_GETVERSION","IMEPADREQ_INSERTSTRING","IMEPADREQ_ISAPPLETACTIVE","IMEPADREQ_ISIMEPADWINDOWVISIBLE","IMEPADREQ_POSTMODALNOTIFY","IMEPADREQ_SENDCONTROL","IMEPADREQ_SETAPPLETMINMAXSIZE","IMEPADREQ_SETAPPLETSIZE","IMEPADREQ_SETAPPLETUISTYLE","Request","Request method [Internationalization for Windows Applications]","Request method [Internationalization for Windows Applications]","IImePad interface","imepad/IImePad::Request","intl.iimepad_request"]
old-location: intl\iimepad_request.htm
tech.root: Intl
ms.assetid: C74B0374-D6C7-44C7-94EF-E97B46534462
ms.date: 12/05/2018
ms.keywords: IImePad interface [Internationalization for Windows Applications],Request method, IImePad.Request, IImePad::Request, IMEPADREQ_CHANGESTRING, IMEPADREQ_DELETESTRING, IMEPADREQ_FORCEIMEPADWINDOWSHOW, IMEPADREQ_GETAPPLETUISTYLE, IMEPADREQ_GETAPPLHWND, IMEPADREQ_GETCOMPOSITIONSTRING, IMEPADREQ_GETCOMPOSITIONSTRINGINFO, IMEPADREQ_GETCONVERSIONSTATUS, IMEPADREQ_GETCURRENTIMEINFO, IMEPADREQ_GETCURRENTUILANG, IMEPADREQ_GETDEFAULTUILANGID, IMEPADREQ_GETVERSION, IMEPADREQ_INSERTSTRING, IMEPADREQ_ISAPPLETACTIVE, IMEPADREQ_ISIMEPADWINDOWVISIBLE, IMEPADREQ_POSTMODALNOTIFY, IMEPADREQ_SENDCONTROL, IMEPADREQ_SETAPPLETMINMAXSIZE, IMEPADREQ_SETAPPLETSIZE, IMEPADREQ_SETAPPLETUISTYLE, Request, Request method [Internationalization for Windows Applications], Request method [Internationalization for Windows Applications],IImePad interface, imepad/IImePad::Request, intl.iimepad_request
req.header: imepad.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImePad::Request
 - imepad/IImePad::Request
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imepad.h
api_name:
 - IImePad.Request
---

# IImePad::Request


## -description

Called by an  <a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a> to insert text into an app.

<b>Request</b> is the only method that <a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a> can call. By calling this method with one of the <b>IMEPADREQ_*</b> request IDs, <b>IImePadApplet</b> can insert text into an app and can control IME's composition string in an  app.

## -parameters

### -param pIImePadApplet [in]

The interface pointer of the calling applet.

### -param reqId [in]

The type of request (the request ID). This must be set to one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_INSERTSTRING"></a><a id="imepadreq_insertstring"></a><dl>
<dt><b>IMEPADREQ_INSERTSTRING</b></dt>
</dl>
</td>
<td width="60%">
Insert a string into the app as a composition string.

<ul>
<li><i>wParam</i>: Pointer to the <b>NULL</b>-terminated string (<b>LPWSTR</b>) to be inserted into the app.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_SENDCONTROL"></a><a id="imepadreq_sendcontrol"></a><dl>
<dt><b>IMEPADREQ_SENDCONTROL</b></dt>
</dl>
</td>
<td width="60%">
Controls composition of the string and caret in the app.

<ul>
<li><i>wParam</i>: Specifies the control value (<b>IMEPADCTRL_*</b>) that requests IME to process the composition string and caret position. See Remarks for a list of the <b>IMEPADCTRL_*</b> values.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_SETAPPLETSIZE"></a><a id="imepadreq_setappletsize"></a><dl>
<dt><b>IMEPADREQ_SETAPPLETSIZE</b></dt>
</dl>
</td>
<td width="60%">
Set a new applet window size.

<ul>
<li><i>wParam</i>: LOWORD(<i>wParam</i>) specifies the applet's width.  HIWORD(<i>wParam</i>) specifies applet's height</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_GETCOMPOSITIONSTRING"></a><a id="imepadreq_getcompositionstring"></a><dl>
<dt><b>IMEPADREQ_GETCOMPOSITIONSTRING</b></dt>
</dl>
</td>
<td width="60%">
Gets the current composition string text.

<ul>
<li><i>wParam</i>: Points to the buffer (<b>LPWSTR</b>) that is to receive the current composition string text.</li>
<li><i>lParam</i>: The maximum number of characters to copy, including the terminating null character.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_GETCOMPOSITIONSTRINGINFO"></a><a id="imepadreq_getcompositionstringinfo"></a><dl>
<dt><b>IMEPADREQ_GETCOMPOSITIONSTRINGINFO</b></dt>
</dl>
</td>
<td width="60%">
Gets information about the current composition string.

<ul>
<li><i>wParam</i>: Pointer to a <a href="/windows/desktop/api/imepad/ns-imepad-imecompositionstringinfo">IMECOMPOSITIONSTRINGINFO</a> structure that receives the composition information.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_DELETESTRING"></a><a id="imepadreq_deletestring"></a><dl>
<dt><b>IMEPADREQ_DELETESTRING</b></dt>
</dl>
</td>
<td width="60%">
Delete the composition string.

<ul>
<li><i>wParam</i>: LOWORD(<i>wParam</i>) specifies the start position of the composition string to be deleted.
HIWORD(<i>wParam</i>)  specifies the length of the composition string to delete. </li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_CHANGESTRING"></a><a id="imepadreq_changestring"></a><dl>
<dt><b>IMEPADREQ_CHANGESTRING</b></dt>
</dl>
</td>
<td width="60%">
Replace part of the composition string.

<ul>
<li><i>wParam</i>: Pointer to the replacement string (<b>LPWSTR</b>).</li>
<li><i>lParam</i>: LOWORD(<i>lParam</i>) specifies the start position of the composition string to be replaced.
HIWORD(<i>lParam</i>) specifies the length of the composition string to be replaced.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_GETAPPLHWND"></a><a id="imepadreq_getapplhwnd"></a><dl>
<dt><b>IMEPADREQ_GETAPPLHWND</b></dt>
</dl>
</td>
<td width="60%">
Gets the application window handle.

<ul>
<li><i>wParam</i>: The <b>HWND</b> handle address (<b>HWND</b> *) to receive the application window handle.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_FORCEIMEPADWINDOWSHOW"></a><a id="imepadreq_forceimepadwindowshow"></a><dl>
<dt><b>IMEPADREQ_FORCEIMEPADWINDOWSHOW</b></dt>
</dl>
</td>
<td width="60%">
Keeps the ImePad window visible.

<ul>
<li><i>wParam</i>: <b>TRUE</b> to keep the IMEPad window visible.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_POSTMODALNOTIFY"></a><a id="imepadreq_postmodalnotify"></a><dl>
<dt><b>IMEPADREQ_POSTMODALNOTIFY</b></dt>
</dl>
</td>
<td width="60%">
Causes <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> to call the applet's <a href="/windows/desktop/api/imepad/nf-imepad-iimepadapplet-notify">Notify</a> method asynchronously with a specific notification Id and user-defined data.

<ul>
<li><i>wParam</i>: The notify code (<b>IMEPN_*</b>). See the Remarks for <a href="/windows/desktop/api/imepad/nf-imepad-iimepadapplet-notify">IImePadApplet::Notify</a> for the possible <b>IMEPN_*</b> codes.</li>
<li><i>lParam</i>: User-defined data</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_GETDEFAULTUILANGID"></a><a id="imepadreq_getdefaultuilangid"></a><dl>
<dt><b>IMEPADREQ_GETDEFAULTUILANGID</b></dt>
</dl>
</td>
<td width="60%">
Gets the recommended (default) ImePad applet UI Language.

<ul>
<li><i>wParam</i>: Address of Language ID (<b>LANGID</b> *) to receive the  default UI Language.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_GETCURRENTUILANG"></a><a id="imepadreq_getcurrentuilang"></a><dl>
<dt><b>IMEPADREQ_GETCURRENTUILANG</b></dt>
</dl>
</td>
<td width="60%">
Get the current ImePad applet UI Language.

<ul>
<li><i>wParam</i>: Address of Language ID (<b>LANGID</b> *) to receive the current UI Language.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_GETAPPLETUISTYLE"></a><a id="imepadreq_getappletuistyle"></a><dl>
<dt><b>IMEPADREQ_GETAPPLETUISTYLE</b></dt>
</dl>
</td>
<td width="60%">
Gets the applet's UI style (<b>IPAWS_*</b> flags).

<ul>
<li><i>wParam</i>: Address to receive the applet UI style (<b>DWORD</b> *). The style is a combination of <b>IPAWS_*</b> flags; see Remarks for the possible <b>IPAWS_*</b> flags.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_SETAPPLETUISTYLE"></a><a id="imepadreq_setappletuistyle"></a><dl>
<dt><b>IMEPADREQ_SETAPPLETUISTYLE</b></dt>
</dl>
</td>
<td width="60%">
Sets the applet's UI style (<b>IPAWS_*</b> flags).

<ul>
<li><i>wParam</i>: Applet UI style. The style is a combination of <b>IPAWS_*</b> flags; see Remarks for the possible <b>IPAWS_*</b> flags.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_ISAPPLETACTIVE"></a><a id="imepadreq_isappletactive"></a><dl>
<dt><b>IMEPADREQ_ISAPPLETACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Determines if the applet is active.

<ul>
<li><i>wParam</i>: Address to receive the value (<b>BOOL</b> *). If it's <b>TRUE</b>, the applet is active; otherwise the applet is not active.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_ISIMEPADWINDOWVISIBLE"></a><a id="imepadreq_isimepadwindowvisible"></a><dl>
<dt><b>IMEPADREQ_ISIMEPADWINDOWVISIBLE</b></dt>
</dl>
</td>
<td width="60%">
Determines if ImePad is visible.

<ul>
<li><i>wParam</i>: Address to receive the value (<b>BOOL</b> *). If it's <b>TRUE</b>, ImePad is visible; otherwise ImePad is not visible.</li>
<li><i>lParam</i>: Not used. Must be set to 0.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_SETAPPLETMINMAXSIZE"></a><a id="imepadreq_setappletminmaxsize"></a><dl>
<dt><b>IMEPADREQ_SETAPPLETMINMAXSIZE</b></dt>
</dl>
</td>
<td width="60%">
Set the minimum and maximum applet size.

<ul>
<li><i>wParam</i>: LOWORD(<i>wParam</i>) specifies the applet width.
HIWORD(<i>wParam</i>) specifies the applet height.</li>
<li><i>lParam</i>: <b>TRUE</b> sets the maximum size; <b>FALSE</b> to sets the  minimum size.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_GETCONVERSIONSTATUS"></a><a id="imepadreq_getconversionstatus"></a><dl>
<dt><b>IMEPADREQ_GETCONVERSIONSTATUS</b></dt>
</dl>
</td>
<td width="60%">
Gets the current application IME's conversion status. For a complete list of conversion and sentence modes, see the header file Imm.h.

<ul>
<li><i>wParam</i>: Address to receive the  conversion mode (<b>DWORD</b> *).</li>
<li><i>lParam</i>: Address to receive the  sentence mode (<b>DWORD</b> *).</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_GETVERSION"></a><a id="imepadreq_getversion"></a><dl>
<dt><b>IMEPADREQ_GETVERSION</b></dt>
</dl>
</td>
<td width="60%">
Gets <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a>'s version information.

<ul>
<li><i>wParam</i>: Address to receive Major version (<b>DWORD</b> *).</li>
<li><i>lParam</i>: Address to receive Minor version (<b>DWORD</b> *).</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="IMEPADREQ_GETCURRENTIMEINFO"></a><a id="imepadreq_getcurrentimeinfo"></a><dl>
<dt><b>IMEPADREQ_GETCURRENTIMEINFO</b></dt>
</dl>
</td>
<td width="60%">
Gets the IME information that invoked ImePad.

<ul>
<li><i>wParam</i>: Address to receive the IME's language ID (<b>DWORD</b> *).</li>
<li><i>lParam</i>: Address to receive the IME's input ID (<b>DWORD</b> *).</li>
</ul>
</td>
</tr>
</table>

### -param wParam [in, out]

Additional information specific to <i>reqId</i>.

### -param lParam [in, out]

Additional information specific to <i>reqId</i>.

## -returns

<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.

## -remarks

<h3><a id="Possible_IMEPADCTRL___values"></a><a id="possible_imepadctrl___values"></a><a id="POSSIBLE_IMEPADCTRL___VALUES"></a>Possible <b>IMEPADCTRL_*</b> values</h3>
These are the possible values that <i>wParam</i> can take when <i>reqId</i> is set to <b>IMEPADREQ_SENDCONTROL</b>:<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>IMEPADCTRL_CONVERTALL</b></td>
<td>1</td>
<td>Convert all composition strings.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_DETERMINALL</b></td>
<td>2</td>
<td>Determine all composition strings.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_DETERMINCHAR</b></td>
<td>3</td>
<td>Determine specified count's composition string character.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_CLEARALL</b></td>
<td>4</td>
<td>Clear all composition strings.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_CARETLEFT</b></td>
<td>6</td>
<td>Move character caret to the left.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_CARETRIGHT</b></td>
<td>7</td>
<td>Move character caret to the right.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_CARETTOP</b></td>
<td>8</td>
<td>Move character caret to the top of the composition string.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_CARETBOTTOM</b></td>
<td>9</td>
<td>Move character caret to the end of the composition string.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_CARETBACKSPACE</b></td>
<td>10</td>
<td>Delete composition string's character before the caret (like the BACKSPACE key).</td>
</tr>
<tr>
<td><b>IMEPADCTRL_CARETDELETE</b></td>
<td>11</td>
<td>Delete composition string's character after the caret (like the DELETE key).</td>
</tr>
<tr>
<td><b>IMEPADCTRL_PHRASEDELETE</b></td>
<td>12</td>
<td>Delete the composition string's phrase.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_INSERTSPACE</b></td>
<td>13</td>
<td>Insert a space character—full width or half width depending on the IME configuration.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_INSERTFULLSPACE</b></td>
<td>14</td>
<td>Insert full width space.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_INSERTHALFSPACE</b></td>
<td>15</td>
<td>Insert half width space.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_ONIME</b></td>
<td>16</td>
<td>Set IME ON.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_OFFIME</b></td>
<td>17</td>
<td>Set IME OFF.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_ONPRECONVERSION</b></td>
<td>18</td>
<td>Set pre-conversion ON.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_OFFPRECONVERSION</b></td>
<td>19</td>
<td>Set pre-conversion OFF.</td>
</tr>
<tr>
<td><b>IMEPADCTRL_PHONETICCANDIDATE</b></td>
<td>20</td>
<td>Open IME's candidate.</td>
</tr>
</table>
 



<h3><a id="Possible_IPAWS___values"></a><a id="possible_ipaws___values"></a><a id="POSSIBLE_IPAWS___VALUES"></a>Possible <b>IPAWS_*</b> values</h3>
These are the possible values that can be received via <i>wParam</i> when <i>reqId</i> is set to <b>IMEPADREQ_GETAPPLETUISTYLE</b>, or that    <i>wParam</i> can be set to when <i>reqId</i> is set to <b>IMEPADREQ_SETAPPLETUISTYLE</b>:<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td><b>IPAWS_ENABLED</b></td>
<td>Show the applet as an enabled window.</td>
</tr>
<tr>
<td><b>IPAWS_SIZINGNOTIFY</b></td>
<td>Send the <b>IMEPN_SIZECHANGING</b> or <b>IMEPN_SIZECHANGED</b> notify code to the applet.</td>
</tr>
<tr>
<td><b>IPAWS_VERTICALFIXED</b></td>
<td>Vertically fixed.</td>
</tr>
<tr>
<td><b>IPAWS_HORIZONTALFIXED</b></td>
<td>Horizontally fixed.</td>
</tr>
<tr>
<td><b>IPAWS_SIZEFIXED</b></td>
<td>Size is fixed.</td>
</tr>
<tr>
<td><b>IPAWS_MAXWIDTHFIXED</b></td>
<td>Max width  is fixed.</td>
</tr>
<tr>
<td><b>IPAWS_MAXHEIGHTFIXED</b></td>
<td>Max height is fixed.</td>
</tr>
<tr>
<td><b>IPAWS_MAXSIZEFIXED</b></td>
<td>Max size is fixed.</td>
</tr>
<tr>
<td><b>IPAWS_MINWIDTHFIXED</b></td>
<td>Min width  is fixed.</td>
</tr>
<tr>
<td><b>IPAWS_MINHEIGHTFIXED</b></td>
<td>Min height is fixed.</td>
</tr>
<tr>
<td><b>IPAWS_MINSIZEFIXED</b></td>
<td>Min size is fixed.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a>



<a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a>



<a href="/windows/desktop/api/imepad/ns-imepad-imecompositionstringinfo">IMECOMPOSITIONSTRINGINFO</a>