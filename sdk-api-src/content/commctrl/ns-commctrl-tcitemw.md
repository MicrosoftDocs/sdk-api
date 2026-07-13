---
UID: NS:commctrl.tagTCITEMW
title: TCITEMW (commctrl.h)
description: Specifies or receives the attributes of a tab item. It is used with the TCM_INSERTITEM, TCM_GETITEM, and TCM_SETITEM messages. This structure supersedes the TC_ITEM structure. (Unicode)
helpviewer_keywords: ["*LPTCITEMW","LPTCITEM","LPTCITEM structure pointer [Windows Controls]","TCIF_IMAGE","TCIF_PARAM","TCIF_RTLREADING","TCIF_STATE","TCIF_TEXT","TCITEM","TCITEM structure [Windows Controls]","TCITEMA","TCITEMW","_win32_TCITEM","_win32_TCITEM_cpp","commctrl/LPTCITEM","commctrl/TCITEM","commctrl/TCITEMA","commctrl/TCITEMW","controls.TCITEM","controls._win32_TCITEM"]
old-location: controls\TCITEM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\structures\tcitem.htm
ms.date: 12/05/2018
ms.keywords: '*LPTCITEMW, LPTCITEM, LPTCITEM structure pointer [Windows Controls], TCIF_IMAGE, TCIF_PARAM, TCIF_RTLREADING, TCIF_STATE, TCIF_TEXT, TCITEM, TCITEM structure [Windows Controls], TCITEMA, TCITEMW, _win32_TCITEM, _win32_TCITEM_cpp, commctrl/LPTCITEM, commctrl/TCITEM, commctrl/TCITEMA, commctrl/TCITEMW, controls.TCITEM, controls._win32_TCITEM'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TCITEMW (Unicode) and TCITEMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TCITEMW, *LPTCITEMW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTCITEMW
 - commctrl/tagTCITEMW
 - LPTCITEMW
 - commctrl/LPTCITEMW
 - TCITEMW
 - commctrl/TCITEMW
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
 - TCITEM
 - TCITEMA
 - TCITEMW
---

## -description

Specifies or receives the attributes of a tab item. It is used with the <a href="/windows/desktop/Controls/tcm-insertitem">TCM_INSERTITEM</a>, <a href="/windows/desktop/Controls/tcm-getitem">TCM_GETITEM</a>, and <a href="/windows/desktop/Controls/tcm-setitem">TCM_SETITEM</a> messages. This structure supersedes the 
			<b>TC_ITEM</b> structure.

## -struct-fields

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Value that specifies which members to retrieve or set. This member can be a combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TCIF_IMAGE"></a><a id="tcif_image"></a><dl>
<dt><b>TCIF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>iImage</b> member is valid. 

</td>
</tr>
<tr>
<td width="40%"><a id="TCIF_PARAM"></a><a id="tcif_param"></a><dl>
<dt><b>TCIF_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The  
						<b>lParam</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TCIF_RTLREADING"></a><a id="tcif_rtlreading"></a><dl>
<dt><b>TCIF_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
The string pointed to by 
						<b>pszText</b> will be displayed in the direction opposite to the text in the parent window.

</td>
</tr>
<tr>
<td width="40%"><a id="TCIF_STATE"></a><a id="tcif_state"></a><dl>
<dt><b>TCIF_STATE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. The 
<b>dwState</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TCIF_TEXT"></a><a id="tcif_text"></a><dl>
<dt><b>TCIF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The <b>pszText</b> member is valid.

</td>
</tr>
</table>

### -field dwState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. Specifies the item's current state if information is being retrieved. If item information is being set, this member contains the state value to be set for the item. For a list of valid tab control item states, see <a href="/windows/desktop/Controls/tab-control-item-states">Tab Control Item States</a>. This member is ignored in the <a href="/windows/desktop/Controls/tcm-insertitem">TCM_INSERTITEM</a> message.

### -field dwStateMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. Specifies which bits of the <b>dwState</b> member contain valid information. This member is ignored in the <a href="/windows/desktop/Controls/tcm-insertitem">TCM_INSERTITEM</a> message.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Pointer to a null-terminated string that contains the tab text when item information is being set. If item information is being retrieved, this member specifies the address of the buffer that receives the tab text.

### -field cchTextMax

Type: <b>int</b>

Size in <b>TCHAR</b><b>s</b> of the buffer pointed to by the 
					<b>pszText</b> member. If the structure is not receiving information, this member is ignored.

### -field iImage

Type: <b>int</b>

Index in the tab control's image list, or -1 if there is no image for the tab.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Application-defined data associated with the tab control item. If more or less than 4 bytes of application-defined data exist per tab, an application must define a structure and use it instead of the <b>TCITEM</b> structure. The first member of the application-defined structure must be a <a href="/windows/desktop/api/commctrl/ns-commctrl-tcitemheadera">TCITEMHEADER</a> structure. 

Typically, windows display text left-to-right (LTR). Windows can be 
				<i>mirrored</i> to display languages such as Hebrew or Arabic that read right-to-left (RTL). Ordinarily, <b>pszText</b> will be displayed in the same direction as the text in its parent window. If TCIF_RTLREADING is set, <b>pszText</b> will read in the opposite direction from the text in the parent window.




> [!NOTE]
> The commctrl.h header defines TCITEM as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
