---
UID: NF:oledlg.IOleUILinkContainerW.GetLinkSource
title: IOleUILinkContainerW::GetLinkSource (oledlg.h)
description: Retrieves information about a link that can be displayed in the Links dialog box. (Unicode)
helpviewer_keywords: ["GetLinkSource","GetLinkSource method [COM]","GetLinkSource method [COM]","IOleUILinkContainer interface","GetLinkSource method [COM]","IOleUILinkContainerA interface","GetLinkSource method [COM]","IOleUILinkContainerW interface","IOleUILinkContainer interface [COM]","GetLinkSource method","IOleUILinkContainer::GetLinkSource","IOleUILinkContainerA interface [COM]","GetLinkSource method","IOleUILinkContainerA::GetLinkSource","IOleUILinkContainerW interface [COM]","GetLinkSource method","IOleUILinkContainerW.GetLinkSource","IOleUILinkContainerW::GetLinkSource","_ole_IOleUILinkContainer_GetLinkSource","com.ioleuilinkcontainer_getlinksource","oledlg/IOleUILinkContainer::GetLinkSource","oledlg/IOleUILinkContainerA::GetLinkSource","oledlg/IOleUILinkContainerW::GetLinkSource"]
old-location: com\ioleuilinkcontainer_getlinksource.htm
tech.root: com
ms.assetid: 10f1bc84-cc09-4a41-8f55-21314338f636
ms.date: 12/05/2018
ms.keywords: GetLinkSource, GetLinkSource method [COM], GetLinkSource method [COM],IOleUILinkContainer interface, GetLinkSource method [COM],IOleUILinkContainerA interface, GetLinkSource method [COM],IOleUILinkContainerW interface, IOleUILinkContainer interface [COM],GetLinkSource method, IOleUILinkContainer::GetLinkSource, IOleUILinkContainerA interface [COM],GetLinkSource method, IOleUILinkContainerA::GetLinkSource, IOleUILinkContainerW interface [COM],GetLinkSource method, IOleUILinkContainerW.GetLinkSource, IOleUILinkContainerW::GetLinkSource, _ole_IOleUILinkContainer_GetLinkSource, com.ioleuilinkcontainer_getlinksource, oledlg/IOleUILinkContainer::GetLinkSource, oledlg/IOleUILinkContainerA::GetLinkSource, oledlg/IOleUILinkContainerW::GetLinkSource
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IOleUILinkContainerW::GetLinkSource
 - oledlg/IOleUILinkContainerW::GetLinkSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleDlg.h
api_name:
 - IOleUILinkContainer.GetLinkSource
 - IOleUILinkContainerA.GetLinkSource
 - IOleUILinkContainerW.GetLinkSource
---

# IOleUILinkContainerW::GetLinkSource


## -description

Retrieves information about a link that can be displayed in the <b>Links</b> dialog box.

## -parameters

### -param dwLink [in]

Container-defined unique identifier for a single link. See <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getnextlink">IOleUILinkContainer::GetNextLink</a>.

### -param lplpszDisplayName [out, optional]

Address of a pointer variable that receives a pointer to the full display name string for the link source. The <b>Links</b> dialog box will free this string.

### -param lplenFileName [out]

Pointer to the length of the leading file name portion of the <i>lplpszDisplayName</i> string. If the link source is not stored in a file, then <i>lplenFileName</i> should be 0. For OLE links, call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-getsourcedisplayname">IOleLink::GetSourceDisplayName</a>.

### -param lplpszFullLinkType [out, optional]

Address of a pointer variable that receives a pointer to the full link type string that is displayed at the bottom of the <b>Links</b> dialog box. The caller allocates this string. The <b>Links</b> dialog box will free this string. For OLE links, this should be the full User Type name. Use <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">IOleObject::GetUserType</a>, specifying USERCLASSTYPE_FULL for <i>dwFormOfType</i>.

### -param lplpszShortLinkType [out, optional]

Address of a pointer variable that receives a pointer to the short link type string that is displayed in the listbox of the <b>Links</b> dialog box. The caller allocates this string. The <b>Links</b> dialog box will free this string. For OLE links, this should be the short user type name. Use <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">IOleObject::GetUserType</a>, specifying USERCLASSTYPE_SHORT for <i>dwFormOfType</i>.

### -param lpfSourceAvailable [out]

Pointer that returns <b>FALSE</b> if it is known that a link is unavailable since the link is to some known but unavailable document. Certain options, such as <b>Update Now</b>, are disabled (grayed in the user interface) for such cases.

### -param lpfIsSelected [out]

Pointer to a variable that tells the <b>Edit Links</b> dialog box that this link's entry should be selected in the dialog's multi-selection listbox. <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a> calls this method at least once for each item to be placed in the links list. If none of them return <b>TRUE</b>, then none of them will be selected when the dialog box is first displayed. If all of them return <b>TRUE</b>, then all will be displayed. That is, it returns <b>TRUE</b> if this link is currently part of the selection in the underlying document, <b>FALSE</b> if not. Any links that are selected in the underlying document are selected in the dialog box; this way, the user can select a set of links and use the dialog box to update them or change their source(s) simultaneously.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Insufficient access permissions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call this method during dialog box initialization, after returning from the <b>Change Source</b> dialog box.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-getsourcedisplayname">IOleLink::GetSourceDisplayName</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">IOleObject::GetUserType</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuichangesourcea">OLEUICHANGESOURCE</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuichangesourcea">OleUIChangeSource</a>



<a href="/windows/desktop/api/oleidl/ne-oleidl-userclasstype">USERCLASSTYPE</a>
