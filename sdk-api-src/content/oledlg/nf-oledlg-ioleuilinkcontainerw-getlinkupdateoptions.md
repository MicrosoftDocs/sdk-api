---
UID: NF:oledlg.IOleUILinkContainerW.GetLinkUpdateOptions
title: IOleUILinkContainerW::GetLinkUpdateOptions (oledlg.h)
description: Determines the current update options for a link. (Unicode)
helpviewer_keywords: ["GetLinkUpdateOptions","GetLinkUpdateOptions method [COM]","GetLinkUpdateOptions method [COM]","IOleUILinkContainer interface","GetLinkUpdateOptions method [COM]","IOleUILinkContainerA interface","GetLinkUpdateOptions method [COM]","IOleUILinkContainerW interface","IOleUILinkContainer interface [COM]","GetLinkUpdateOptions method","IOleUILinkContainer::GetLinkUpdateOptions","IOleUILinkContainerA interface [COM]","GetLinkUpdateOptions method","IOleUILinkContainerA::GetLinkUpdateOptions","IOleUILinkContainerW interface [COM]","GetLinkUpdateOptions method","IOleUILinkContainerW.GetLinkUpdateOptions","IOleUILinkContainerW::GetLinkUpdateOptions","_ole_IOleUILinkContainer_GetLinkUpdateOptions","com.ioleuilinkcontainer_getlinkupdateoptions","oledlg/IOleUILinkContainer::GetLinkUpdateOptions","oledlg/IOleUILinkContainerA::GetLinkUpdateOptions","oledlg/IOleUILinkContainerW::GetLinkUpdateOptions"]
old-location: com\ioleuilinkcontainer_getlinkupdateoptions.htm
tech.root: com
ms.assetid: 136894a6-ddf6-4a47-80f5-997625362536
ms.date: 12/05/2018
ms.keywords: GetLinkUpdateOptions, GetLinkUpdateOptions method [COM], GetLinkUpdateOptions method [COM],IOleUILinkContainer interface, GetLinkUpdateOptions method [COM],IOleUILinkContainerA interface, GetLinkUpdateOptions method [COM],IOleUILinkContainerW interface, IOleUILinkContainer interface [COM],GetLinkUpdateOptions method, IOleUILinkContainer::GetLinkUpdateOptions, IOleUILinkContainerA interface [COM],GetLinkUpdateOptions method, IOleUILinkContainerA::GetLinkUpdateOptions, IOleUILinkContainerW interface [COM],GetLinkUpdateOptions method, IOleUILinkContainerW.GetLinkUpdateOptions, IOleUILinkContainerW::GetLinkUpdateOptions, _ole_IOleUILinkContainer_GetLinkUpdateOptions, com.ioleuilinkcontainer_getlinkupdateoptions, oledlg/IOleUILinkContainer::GetLinkUpdateOptions, oledlg/IOleUILinkContainerA::GetLinkUpdateOptions, oledlg/IOleUILinkContainerW::GetLinkUpdateOptions
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
 - IOleUILinkContainerW::GetLinkUpdateOptions
 - oledlg/IOleUILinkContainerW::GetLinkUpdateOptions
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
 - IOleUILinkContainer.GetLinkUpdateOptions
 - IOleUILinkContainerA.GetLinkUpdateOptions
 - IOleUILinkContainerW.GetLinkUpdateOptions
---

# IOleUILinkContainerW::GetLinkUpdateOptions


## -description

Determines the current update options for a link.

## -parameters

### -param dwLink [in]

Container-defined unique identifier for a single link. See <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getnextlink">IOleUILinkContainer::GetNextLink</a>.

### -param lpdwUpdateOpt [out]

A pointer to the location that the current update options will be written.

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

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Containers can implement this method for OLE links simply by calling <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setupdateoptions">IOleLink::SetUpdateOptions</a> on the link object.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setupdateoptions">IOleLink::SetUpdateOptions</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getnextlink">IOleUILinkContainer::GetNextLink</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-setlinkupdateoptions">IOleUILinkContainer::SetLinkUpdateOptions</a>
