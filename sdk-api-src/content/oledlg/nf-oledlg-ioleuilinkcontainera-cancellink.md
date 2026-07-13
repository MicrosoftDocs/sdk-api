---
UID: NF:oledlg.IOleUILinkContainerA.CancelLink
title: IOleUILinkContainerA::CancelLink (oledlg.h)
description: Disconnects the selected links. (ANSI)
helpviewer_keywords: ["CancelLink","CancelLink method [COM]","CancelLink method [COM]","IOleUILinkContainer interface","CancelLink method [COM]","IOleUILinkContainerA interface","CancelLink method [COM]","IOleUILinkContainerW interface","IOleUILinkContainer interface [COM]","CancelLink method","IOleUILinkContainer::CancelLink","IOleUILinkContainerA interface [COM]","CancelLink method","IOleUILinkContainerA.CancelLink","IOleUILinkContainerA::CancelLink","IOleUILinkContainerW interface [COM]","CancelLink method","IOleUILinkContainerW::CancelLink","_ole_IOleUILinkContainer_CancelLink","com.ioleuilinkcontainer_cancellink","oledlg/IOleUILinkContainer::CancelLink","oledlg/IOleUILinkContainerA::CancelLink","oledlg/IOleUILinkContainerW::CancelLink"]
old-location: com\ioleuilinkcontainer_cancellink.htm
tech.root: com
ms.assetid: 97099e4d-20ea-47fb-8ca8-27330f980038
ms.date: 12/05/2018
ms.keywords: CancelLink, CancelLink method [COM], CancelLink method [COM],IOleUILinkContainer interface, CancelLink method [COM],IOleUILinkContainerA interface, CancelLink method [COM],IOleUILinkContainerW interface, IOleUILinkContainer interface [COM],CancelLink method, IOleUILinkContainer::CancelLink, IOleUILinkContainerA interface [COM],CancelLink method, IOleUILinkContainerA.CancelLink, IOleUILinkContainerA::CancelLink, IOleUILinkContainerW interface [COM],CancelLink method, IOleUILinkContainerW::CancelLink, _ole_IOleUILinkContainer_CancelLink, com.ioleuilinkcontainer_cancellink, oledlg/IOleUILinkContainer::CancelLink, oledlg/IOleUILinkContainerA::CancelLink, oledlg/IOleUILinkContainerW::CancelLink
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
 - IOleUILinkContainerA::CancelLink
 - oledlg/IOleUILinkContainerA::CancelLink
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
 - IOleUILinkContainer.CancelLink
 - IOleUILinkContainerA.CancelLink
 - IOleUILinkContainerW.CancelLink
---

# IOleUILinkContainerA::CancelLink


## -description

Disconnects the selected links.

## -parameters

### -param dwLink

Container-defined unique identifier for a single link. Containers can use the pointer to the link's container site for this value.

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
Call <b>IOleUILinkContainer::CancelLink</b> when the user selects the <b>Break Link</b> button from the <b>Links</b> dialog box. The link should be converted to a picture. The <b>Links</b> dialog box will not be dismissed for OLE links.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
For OLE links, <a href="/windows/desktop/api/ole2/nf-ole2-olecreatestaticfromdata">OleCreateStaticFromData</a> can be used to create a static picture object using the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface of the link as the source.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatestaticfromdata">OleCreateStaticFromData</a>
