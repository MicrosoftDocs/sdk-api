---
UID: NF:oledlg.IOleUILinkContainerW.OpenLinkSource
title: IOleUILinkContainerW::OpenLinkSource (oledlg.h)
description: Opens the link's source. (Unicode)
helpviewer_keywords: ["IOleUILinkContainer interface [COM]","OpenLinkSource method","IOleUILinkContainer::OpenLinkSource","IOleUILinkContainerA interface [COM]","OpenLinkSource method","IOleUILinkContainerA::OpenLinkSource","IOleUILinkContainerW interface [COM]","OpenLinkSource method","IOleUILinkContainerW.OpenLinkSource","IOleUILinkContainerW::OpenLinkSource","OpenLinkSource","OpenLinkSource method [COM]","OpenLinkSource method [COM]","IOleUILinkContainer interface","OpenLinkSource method [COM]","IOleUILinkContainerA interface","OpenLinkSource method [COM]","IOleUILinkContainerW interface","_ole_IOleUILinkContainer_OpenLinkSource","com.ioleuilinkcontainer_openlinksource","oledlg/IOleUILinkContainer::OpenLinkSource","oledlg/IOleUILinkContainerA::OpenLinkSource","oledlg/IOleUILinkContainerW::OpenLinkSource"]
old-location: com\ioleuilinkcontainer_openlinksource.htm
tech.root: com
ms.assetid: bc732a2f-f13d-4d08-a81d-292dd2ba1140
ms.date: 12/05/2018
ms.keywords: IOleUILinkContainer interface [COM],OpenLinkSource method, IOleUILinkContainer::OpenLinkSource, IOleUILinkContainerA interface [COM],OpenLinkSource method, IOleUILinkContainerA::OpenLinkSource, IOleUILinkContainerW interface [COM],OpenLinkSource method, IOleUILinkContainerW.OpenLinkSource, IOleUILinkContainerW::OpenLinkSource, OpenLinkSource, OpenLinkSource method [COM], OpenLinkSource method [COM],IOleUILinkContainer interface, OpenLinkSource method [COM],IOleUILinkContainerA interface, OpenLinkSource method [COM],IOleUILinkContainerW interface, _ole_IOleUILinkContainer_OpenLinkSource, com.ioleuilinkcontainer_openlinksource, oledlg/IOleUILinkContainer::OpenLinkSource, oledlg/IOleUILinkContainerA::OpenLinkSource, oledlg/IOleUILinkContainerW::OpenLinkSource
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
 - IOleUILinkContainerW::OpenLinkSource
 - oledlg/IOleUILinkContainerW::OpenLinkSource
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
 - IOleUILinkContainer.OpenLinkSource
 - IOleUILinkContainerA.OpenLinkSource
 - IOleUILinkContainerW.OpenLinkSource
---

# IOleUILinkContainerW::OpenLinkSource


## -description

Opens the link's source.

## -parameters

### -param dwLink [in]

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
The <b>IOleUILinkContainer::OpenLinkSource</b> method is called when the <b>Open Source</b> button is selected from the <b>Links</b> dialog box. For OLE links, call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a>, specifying OLEIVERB_SHOW for <i>iVerb</i>.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oleidl/ns-oleidl-oleverb">OLEVERB</a>
