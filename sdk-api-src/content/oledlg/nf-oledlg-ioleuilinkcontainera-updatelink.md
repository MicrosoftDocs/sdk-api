---
UID: NF:oledlg.IOleUILinkContainerA.UpdateLink
title: IOleUILinkContainerA::UpdateLink (oledlg.h)
description: Forces selected links to connect to their source and retrieve current information. (ANSI)
helpviewer_keywords: ["IOleUILinkContainer interface [COM]","UpdateLink method","IOleUILinkContainer::UpdateLink","IOleUILinkContainerA interface [COM]","UpdateLink method","IOleUILinkContainerA.UpdateLink","IOleUILinkContainerA::UpdateLink","IOleUILinkContainerW interface [COM]","UpdateLink method","IOleUILinkContainerW::UpdateLink","UpdateLink","UpdateLink method [COM]","UpdateLink method [COM]","IOleUILinkContainer interface","UpdateLink method [COM]","IOleUILinkContainerA interface","UpdateLink method [COM]","IOleUILinkContainerW interface","_ole_IOleUILinkContainer_UpdateLink","com.ioleuilinkcontainer_updatelink","oledlg/IOleUILinkContainer::UpdateLink","oledlg/IOleUILinkContainerA::UpdateLink","oledlg/IOleUILinkContainerW::UpdateLink"]
old-location: com\ioleuilinkcontainer_updatelink.htm
tech.root: com
ms.assetid: fccee32a-3a6f-4ef8-9ca7-c5b664ee03cf
ms.date: 12/05/2018
ms.keywords: IOleUILinkContainer interface [COM],UpdateLink method, IOleUILinkContainer::UpdateLink, IOleUILinkContainerA interface [COM],UpdateLink method, IOleUILinkContainerA.UpdateLink, IOleUILinkContainerA::UpdateLink, IOleUILinkContainerW interface [COM],UpdateLink method, IOleUILinkContainerW::UpdateLink, UpdateLink, UpdateLink method [COM], UpdateLink method [COM],IOleUILinkContainer interface, UpdateLink method [COM],IOleUILinkContainerA interface, UpdateLink method [COM],IOleUILinkContainerW interface, _ole_IOleUILinkContainer_UpdateLink, com.ioleuilinkcontainer_updatelink, oledlg/IOleUILinkContainer::UpdateLink, oledlg/IOleUILinkContainerA::UpdateLink, oledlg/IOleUILinkContainerW::UpdateLink
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
 - IOleUILinkContainerA::UpdateLink
 - oledlg/IOleUILinkContainerA::UpdateLink
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
 - IOleUILinkContainer.UpdateLink
 - IOleUILinkContainerA.UpdateLink
 - IOleUILinkContainerW.UpdateLink
---

# IOleUILinkContainerA::UpdateLink


## -description

Forces selected links to connect to their source and retrieve current information.

## -parameters

### -param dwLink [in]

Container-defined unique identifier for a single link. Containers can use the pointer to the link's container site for this value.

### -param fErrorMessage [in]

Determines whether the caller (implementer of <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>) should show an error message upon failure to update a link. The <b>Update Links</b> dialog box sets this to <b>FALSE</b>. The <b>Object Properties</b> and <b>Links</b> dialog boxes set it to <b>TRUE</b>.

### -param fReserved [in]

This parameter is reserved and must be set to <b>FALSE</b>.

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
Call this method with <i>fErrorMessage</i> set to <b>TRUE</b> in cases where the user expressly presses a button to have a link updated, that is, presses the links' <b>Update Now</b> button. Call it with <b>FALSE</b> in cases where the container should never display an error message, that is, where a large set of operations are being performed and the error should be propagated back to the user later, as might occur with the <b>Update links</b> progress meter. Rather than providing one message for each failure, assuming there are failures, provide a single message for all failures at the end of the operation.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
For OLE links, call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-update">IOleObject::Update</a>.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-update">IOleObject::Update</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>
