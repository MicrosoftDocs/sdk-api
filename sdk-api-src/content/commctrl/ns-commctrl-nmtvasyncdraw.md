---
UID: NS:commctrl.tagNMTVASYNCDRAW
title: NMTVASYNCDRAW (commctrl.h)
description: Contains an explanation of why the draw of an icon or overlay tree item failed.
helpviewer_keywords: ["ADRF_DRAWIMAGE","ADRF_DRAWNOTHING","ADRF_DRAWSYNC","NMTVASYNCDRAW","NMTVASYNCDRAW structure [Windows Controls]","_shell_NMTVASYNCDRAW","_shell_NMTVASYNCDRAW_cpp","commctrl/NMTVASYNCDRAW","controls.NMTVASYNCDRAW","controls._shell_NMTVASYNCDRAW"]
old-location: controls\NMTVASYNCDRAW.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvasyncdraw.htm
ms.date: 12/05/2018
ms.keywords: ADRF_DRAWIMAGE, ADRF_DRAWNOTHING, ADRF_DRAWSYNC, NMTVASYNCDRAW, NMTVASYNCDRAW structure [Windows Controls], _shell_NMTVASYNCDRAW, _shell_NMTVASYNCDRAW_cpp, commctrl/NMTVASYNCDRAW, controls.NMTVASYNCDRAW, controls._shell_NMTVASYNCDRAW
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: NMTVASYNCDRAW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMTVASYNCDRAW
 - commctrl/tagNMTVASYNCDRAW
 - NMTVASYNCDRAW
 - commctrl/NMTVASYNCDRAW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMTVASYNCDRAW
---

# NMTVASYNCDRAW structure


## -description

Contains an explanation of why the draw of an icon or overlay tree item failed. This structure is sent on a <a href="/windows/desktop/Controls/tvn-asyncdraw">TVN_ASYNCDRAW</a> notification. Set the <b>dwRetFlags</b> member to indicate what action the control should take. Note that a draw can fail if there is no image; in other words, when the icon image has not been extracted.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure.

### -field pimldp

Type: <b><a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imagelistdrawparams">IMAGELISTDRAWPARAMS</a>*</b>


<a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imagelistdrawparams">IMAGELISTDRAWPARAMS</a> structure describing the image that failed to draw.

### -field hr

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Result code indicating why the draw failed, either ILDRF_IMAGELOWQUALITY, ILDRF_OVERLAYLOWQUALITY, E_PENDING, or S_OK. A code of S_OK indicates that the image is present but not at the required image quality.

### -field hItem

Type: <b>HTREEITEM</b>

Handle of the tree item that failed to draw.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Data for <b>hItem</b>. This is the same data for the item that is retrieved with the message <a href="/windows/desktop/Controls/tvm-getitem">TVM_GETITEM</a> using the appropriate <b>mask</b> in structure <a href="/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a>. This data is parent specific; the parent can store information that helps it identify the tree item or other information. Data is provided in <b>lParam</b> for convenience, so that the parent does not need to send message <b>TVM_GETITEM</b>.

### -field dwRetFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Action that the sender (the tree-view control) should execute on return. Value must be one of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADRF_DRAWIMAGE"></a><a id="adrf_drawimage"></a><dl>
<dt><b>ADRF_DRAWIMAGE</b></dt>
</dl>
</td>
<td width="60%">
Draw the image specified by <b>iRetImageIndex</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="ADRF_DRAWSYNC"></a><a id="adrf_drawsync"></a><dl>
<dt><b>ADRF_DRAWSYNC</b></dt>
</dl>
</td>
<td width="60%">
Proceed to draw the image anyway, that is, synchronously extract the image and paint. Assuming the control is on the UI thread, use of this flag implies low priority UI performance, since extraction times may vary and the UI could be unresponsive for an extended period of time during extraction.

</td>
</tr>
<tr>
<td width="40%"><a id="ADRF_DRAWNOTHING"></a><a id="adrf_drawnothing"></a><dl>
<dt><b>ADRF_DRAWNOTHING</b></dt>
</dl>
</td>
<td width="60%">
Do not draw an image.

</td>
</tr>
</table>

### -field iRetImageIndex

Type: <b>int</b>

Index of the image to draw in the image list. Used if ADRF_DRAWIMAGE is returned in <b>dwRetFlags</b>.