---
UID: NF:oleidl.IOleLink.GetSourceMoniker
title: IOleLink::GetSourceMoniker (oleidl.h)
description: Retrieves the moniker identifying the link source of a linked object.
helpviewer_keywords: ["GetSourceMoniker","GetSourceMoniker method [COM]","GetSourceMoniker method [COM]","IOleLink interface","IOleLink interface [COM]","GetSourceMoniker method","IOleLink.GetSourceMoniker","IOleLink::GetSourceMoniker","_ole_iolelink_getsourcemoniker","com.iolelink_getsourcemoniker","oleidl/IOleLink::GetSourceMoniker"]
old-location: com\iolelink_getsourcemoniker.htm
tech.root: com
ms.assetid: ef447726-7aef-45c4-a522-a8de9a3e6b74
ms.date: 12/05/2018
ms.keywords: GetSourceMoniker, GetSourceMoniker method [COM], GetSourceMoniker method [COM],IOleLink interface, IOleLink interface [COM],GetSourceMoniker method, IOleLink.GetSourceMoniker, IOleLink::GetSourceMoniker, _ole_iolelink_getsourcemoniker, com.iolelink_getsourcemoniker, oleidl/IOleLink::GetSourceMoniker
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IOleLink::GetSourceMoniker
 - oleidl/IOleLink::GetSourceMoniker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleLink.GetSourceMoniker
---

# IOleLink::GetSourceMoniker


## -description

Retrieves the moniker identifying the link source of a linked object.

## -parameters

### -param ppmk [out]

Address of an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> pointer variable that receives the interface pointer to an absolute moniker that identifies the link source. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on <i>ppmk</i>; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs the implementation must set <i>ppmk</i> to <b>NULL</b>.

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
<dt><b>MK_E_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No moniker is available.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Your container application can call <b>IOleLink::GetSourceMoniker</b> to display the current source of a link in the <b>Links</b> dialog box. Note that this requires your container to use the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-getdisplayname">IMoniker::GetDisplayName</a> method to get the display name of the moniker. If you would rather get the display name directly, your container can call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-getsourcedisplayname">IOleLink::GetSourceDisplayName</a> instead of <b>IOleLink::GetSourceMoniker</b>.

If you use the <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a> function to display the <b>Links</b> dialog box, you must implement the <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a> interface. The dialog box calls your implementations of <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-getlinksource">IOleUILinkContainer::GetLinkSource</a> to get the string it should display. Your implementation of that method can call <b>IOleLink::GetSourceMoniker</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The linked object stores both an absolute and a relative moniker for the link source. If the relative moniker is non-<b>NULL</b> and a moniker is available for the compound document, <b>IOleLink::GetSourceMoniker</b> returns the moniker created by composing the relative moniker onto the end of the compound document's moniker. Otherwise, it returns the absolute moniker or, if an error occurs, <b>NULL</b>.

The container specifies the absolute moniker when it calls one of the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelink">OleCreateLink</a> functions to create a link. The application can call <b>IOleLink::GetSourceMoniker</b> or <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-getsourcedisplayname">IOleLink::GetSourceDisplayName</a> to change the absolute moniker. In addition, the linked object automatically updates the monikers whenever it successfully binds to the link source, or when it is bound to the link source and it receives a rename notification through the <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onrename">IAdviseSink::OnRename</a> method.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-getsourcedisplayname">IOleLink::GetSourceDisplayName</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-getsourcemoniker">IOleLink::GetSourceMoniker</a>