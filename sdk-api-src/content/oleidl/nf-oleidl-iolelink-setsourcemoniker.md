---
UID: NF:oleidl.IOleLink.SetSourceMoniker
title: IOleLink::SetSourceMoniker (oleidl.h)
description: Sets the moniker for the link source.
helpviewer_keywords: ["IOleLink interface [COM]","SetSourceMoniker method","IOleLink.SetSourceMoniker","IOleLink::SetSourceMoniker","SetSourceMoniker","SetSourceMoniker method [COM]","SetSourceMoniker method [COM]","IOleLink interface","_ole_iolelink_setsourcemoniker","com.iolelink_setsourcemoniker","oleidl/IOleLink::SetSourceMoniker"]
old-location: com\iolelink_setsourcemoniker.htm
tech.root: com
ms.assetid: 85fe1d28-d9c6-46b4-abff-6afce9ff3cd0
ms.date: 12/05/2018
ms.keywords: IOleLink interface [COM],SetSourceMoniker method, IOleLink.SetSourceMoniker, IOleLink::SetSourceMoniker, SetSourceMoniker, SetSourceMoniker method [COM], SetSourceMoniker method [COM],IOleLink interface, _ole_iolelink_setsourcemoniker, com.iolelink_setsourcemoniker, oleidl/IOleLink::SetSourceMoniker
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
 - IOleLink::SetSourceMoniker
 - oleidl/IOleLink::SetSourceMoniker
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
 - IOleLink.SetSourceMoniker
---

# IOleLink::SetSourceMoniker


## -description

Sets the moniker for the link source.

## -parameters

### -param pmk [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on a moniker that identifies the new link source of the linked object. A value of <b>NULL</b> breaks the link.

### -param rclsid [in]

The CLSID of the link source that the linked object should use to access information about the linked object when it is not bound.

## -returns

This method returns S_OK on success.

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Your container application can call <b>IOleLink::SetSourceMoniker</b> when the end user changes the source of a link or breaks a link. Note that this requires your container to use the <a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a> function to create a moniker out of the display name that the end user enters. If you'd rather have the linked object perform the parsing, your container can call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setsourcedisplayname">IOleLink::SetSourceDisplayName</a> instead of <b>IOleLink::SetSourceMoniker</b>.

The end user changes the source of a link or breaks a link using the <b>Links</b> dialog box. If you use the <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a> function to display the <b>Links</b> dialog box, you must implement the <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a> interface. The dialog box calls your implementations of <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-setlinksource">IOleUILinkContainer::SetLinkSource</a> and <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-cancellink">IOleUILinkContainer::CancelLink</a>; your implementation of these methods can call <b>IOleLink::SetSourceMoniker</b>.

If the linked object is currently bound to its link source, the linked object's implementation of <b>IOleLink::SetSourceMoniker</b> closes the link before changing the moniker.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The <a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a> contract does not specify how the linked object stores or uses the link source moniker. The provided implementation stores the absolute moniker specified when the link is created or when the moniker is changed; it then computes and stores a relative moniker. Future implementations might manage monikers differently to provide better moniker tracking. The absolute moniker provides the complete path to the link source. The linked object uses this absolute moniker and the moniker of the compound document to compute a relative moniker that identifies the link source relative to the compound document that contains the link.

pmkCompoundDoc-&gt;RelativePathTo(pmkAbsolute, ppmkRelative)

When binding to the link source, the linked object first tries to bind using the relative moniker. If that fails, it tries to bind the absolute moniker.

When the linked object successfully binds using either the relative or the absolute moniker, it automatically updates the other moniker. The linked object also updates both monikers when it is bound to the link source and it receives a rename notification through the <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onrename">IAdviseSink::OnRename</a> method. A container application can also use the <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setsourcedisplayname">IOleLink::SetSourceDisplayName</a> method to change a link's moniker.

The linked object's implementation of <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a> saves both the relative and the absolute moniker.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-getsourcemoniker">IOleLink::GetSourceMoniker</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setsourcedisplayname">IOleLink::SetSourceDisplayName</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a>