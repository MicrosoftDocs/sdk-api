---
UID: NF:oledlg.IOleUILinkContainerW.SetLinkUpdateOptions
title: IOleUILinkContainerW::SetLinkUpdateOptions (oledlg.h)
description: Sets a link's update options to automatic or manual. (Unicode)
helpviewer_keywords: ["IOleUILinkContainer interface [COM]","SetLinkUpdateOptions method","IOleUILinkContainer::SetLinkUpdateOptions","IOleUILinkContainerA interface [COM]","SetLinkUpdateOptions method","IOleUILinkContainerA::SetLinkUpdateOptions","IOleUILinkContainerW interface [COM]","SetLinkUpdateOptions method","IOleUILinkContainerW.SetLinkUpdateOptions","IOleUILinkContainerW::SetLinkUpdateOptions","SetLinkUpdateOptions","SetLinkUpdateOptions method [COM]","SetLinkUpdateOptions method [COM]","IOleUILinkContainer interface","SetLinkUpdateOptions method [COM]","IOleUILinkContainerA interface","SetLinkUpdateOptions method [COM]","IOleUILinkContainerW interface","_ole_IOleUILinkContainer_SetLinkUpdateOptions","com.ioleuilinkcontainer_setlinkupdateoptions","oledlg/IOleUILinkContainer::SetLinkUpdateOptions","oledlg/IOleUILinkContainerA::SetLinkUpdateOptions","oledlg/IOleUILinkContainerW::SetLinkUpdateOptions"]
old-location: com\ioleuilinkcontainer_setlinkupdateoptions.htm
tech.root: com
ms.assetid: d2a7758d-9692-4e3c-8186-b74530299a6a
ms.date: 12/05/2018
ms.keywords: IOleUILinkContainer interface [COM],SetLinkUpdateOptions method, IOleUILinkContainer::SetLinkUpdateOptions, IOleUILinkContainerA interface [COM],SetLinkUpdateOptions method, IOleUILinkContainerA::SetLinkUpdateOptions, IOleUILinkContainerW interface [COM],SetLinkUpdateOptions method, IOleUILinkContainerW.SetLinkUpdateOptions, IOleUILinkContainerW::SetLinkUpdateOptions, SetLinkUpdateOptions, SetLinkUpdateOptions method [COM], SetLinkUpdateOptions method [COM],IOleUILinkContainer interface, SetLinkUpdateOptions method [COM],IOleUILinkContainerA interface, SetLinkUpdateOptions method [COM],IOleUILinkContainerW interface, _ole_IOleUILinkContainer_SetLinkUpdateOptions, com.ioleuilinkcontainer_setlinkupdateoptions, oledlg/IOleUILinkContainer::SetLinkUpdateOptions, oledlg/IOleUILinkContainerA::SetLinkUpdateOptions, oledlg/IOleUILinkContainerW::SetLinkUpdateOptions
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
 - IOleUILinkContainerW::SetLinkUpdateOptions
 - oledlg/IOleUILinkContainerW::SetLinkUpdateOptions
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
 - IOleUILinkContainer.SetLinkUpdateOptions
 - IOleUILinkContainerA.SetLinkUpdateOptions
 - IOleUILinkContainerW.SetLinkUpdateOptions
---

# IOleUILinkContainerW::SetLinkUpdateOptions


## -description

Sets a link's update options to automatic or manual.

## -parameters

### -param dwLink [in]

Container-defined unique identifier for a single link. See <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getnextlink">IOleUILinkContainer::GetNextLink</a>.

### -param dwUpdateOpt [in]

Update options, which can be automatic (OLEUPDATE_ALWAYS) or manual (OLEUPDATE_ONCALL).

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
Containers can implement this method for OLE links by simply calling <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setupdateoptions">IOleLink::SetUpdateOptions</a> on the link object.

## -see-also

<b>IOleLink::SetUpdateOptions</b>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getnextlink">IOleUILinkContainer::GetNextLink</a>
