---
UID: NF:oledlg.IOleUILinkContainerW.SetLinkSource
title: IOleUILinkContainerW::SetLinkSource (oledlg.h)
description: Changes the source of a link. (Unicode)
helpviewer_keywords: ["IOleUILinkContainer interface [COM]","SetLinkSource method","IOleUILinkContainer::SetLinkSource","IOleUILinkContainerA interface [COM]","SetLinkSource method","IOleUILinkContainerA::SetLinkSource","IOleUILinkContainerW interface [COM]","SetLinkSource method","IOleUILinkContainerW.SetLinkSource","IOleUILinkContainerW::SetLinkSource","SetLinkSource","SetLinkSource method [COM]","SetLinkSource method [COM]","IOleUILinkContainer interface","SetLinkSource method [COM]","IOleUILinkContainerA interface","SetLinkSource method [COM]","IOleUILinkContainerW interface","com.ioleuilinkcontainer_setlinksource","ole_IOleUILinkContainer_SetLinkSource","oledlg/IOleUILinkContainer::SetLinkSource","oledlg/IOleUILinkContainerA::SetLinkSource","oledlg/IOleUILinkContainerW::SetLinkSource"]
old-location: com\ioleuilinkcontainer_setlinksource.htm
tech.root: com
ms.assetid: c76723e8-e895-4ba1-9ba1-7e56a44cc5f2
ms.date: 12/05/2018
ms.keywords: IOleUILinkContainer interface [COM],SetLinkSource method, IOleUILinkContainer::SetLinkSource, IOleUILinkContainerA interface [COM],SetLinkSource method, IOleUILinkContainerA::SetLinkSource, IOleUILinkContainerW interface [COM],SetLinkSource method, IOleUILinkContainerW.SetLinkSource, IOleUILinkContainerW::SetLinkSource, SetLinkSource, SetLinkSource method [COM], SetLinkSource method [COM],IOleUILinkContainer interface, SetLinkSource method [COM],IOleUILinkContainerA interface, SetLinkSource method [COM],IOleUILinkContainerW interface, com.ioleuilinkcontainer_setlinksource, ole_IOleUILinkContainer_SetLinkSource, oledlg/IOleUILinkContainer::SetLinkSource, oledlg/IOleUILinkContainerA::SetLinkSource, oledlg/IOleUILinkContainerW::SetLinkSource
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
 - IOleUILinkContainerW::SetLinkSource
 - oledlg/IOleUILinkContainerW::SetLinkSource
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
 - IOleUILinkContainer.SetLinkSource
 - IOleUILinkContainerA.SetLinkSource
 - IOleUILinkContainerW.SetLinkSource
---

# IOleUILinkContainerW::SetLinkSource


## -description

Changes the source of a link.

## -parameters

### -param dwLink [in]

Container-defined unique identifier for a single link. See <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getnextlink">IOleUILinkContainer::GetNextLink</a>.

### -param lpszDisplayName [in]

Pointer to new source string to be parsed.

### -param lenFileName [in]

Length of the leading file name portion of the <i>lpszDisplayName</i> string. If the link source is not stored in a file, then <i>lenFileName</i> should be 0. For OLE links, call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-getsourcedisplayname">IOleLink::GetSourceDisplayName</a>.

### -param pchEaten [out]

Pointer to the number of characters successfully parsed in <i>lpszDisplayName</i>.

### -param fValidateSource [in]

<b>TRUE</b> if the moniker should be validated; for OLE links, <a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a> should be called. <b>FALSE</b> if the moniker should not be validated. If possible, the link should accept the unvalidated source, and mark itself as unavailable.

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
The supplied identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call this method from the <b>Change Source</b> dialog box, with <i>fValidateSource</i> initially set to <b>TRUE</b>. <b>Change Source</b> can be called directly or from the <b>Links</b> dialog box. If this call to <b>IOleUILinkContainer::SetLinkSource</b> returns an error (e.g., <a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a> failed because the source was unavailable), then you should display an <b>Invalid Link Source</b> message, and the user should be allowed to decide whether to fix the source. If the user chooses to fix the source, then the user should be returned to the <b>Change Source</b> dialog box with the invalid portion of the input string highlighted. If the user chooses not to fix the source, then <b>IOleUILinkContainer::SetLinkSource</b> should be called a second time with <i>fValidateSource</i> set to <b>FALSE</b>, and the user should be returned to the <b>Links</b> dialog box with the link marked <b>Unavailable</b>.

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a>
