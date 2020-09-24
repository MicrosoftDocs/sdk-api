---
UID: NF:oleidl.IOleLink.SetSourceDisplayName
title: IOleLink::SetSourceDisplayName (oleidl.h)
description: Sets the display name for the link source.
helpviewer_keywords: ["IOleLink interface [COM]","SetSourceDisplayName method","IOleLink.SetSourceDisplayName","IOleLink::SetSourceDisplayName","SetSourceDisplayName","SetSourceDisplayName method [COM]","SetSourceDisplayName method [COM]","IOleLink interface","_ole_iolelink_setsourcedisplayname","com.iolelink_setsourcedisplayname","oleidl/IOleLink::SetSourceDisplayName"]
old-location: com\iolelink_setsourcedisplayname.htm
tech.root: com
ms.assetid: 762d021f-4bf1-4f90-bf41-065b8810de47
ms.date: 12/05/2018
ms.keywords: IOleLink interface [COM],SetSourceDisplayName method, IOleLink.SetSourceDisplayName, IOleLink::SetSourceDisplayName, SetSourceDisplayName, SetSourceDisplayName method [COM], SetSourceDisplayName method [COM],IOleLink interface, _ole_iolelink_setsourcedisplayname, com.iolelink_setsourcedisplayname, oleidl/IOleLink::SetSourceDisplayName
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
 - IOleLink::SetSourceDisplayName
 - oleidl/IOleLink::SetSourceDisplayName
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
 - IOleLink.SetSourceDisplayName
---

# IOleLink::SetSourceDisplayName


## -description

Sets the display name for the link source.

## -parameters

### -param pszStatusText [in]

A pointer to the display name of the new link source. This parameter cannot be <b>NULL</b>.

## -returns

This method returns S_OK on success.

Values from <a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a> may also be returned here.

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Your container application can call <b>IOleLink::SetSourceDisplayName</b> when the end user changes the source of a link or breaks a link. Note that this requires the linked object to create a moniker out of the display name. If you'd rather parse the display name into a moniker yourself, your container can call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setsourcemoniker">IOleLink::SetSourceMoniker</a> instead of <b>IOleLink::SetSourceDisplayName</b>.

If you use the <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a> function to display the <b>Links</b> dialog box, you must implement the <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a> interface. The dialog box calls your implementations of <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-setlinksource">IOleUILinkContainer::SetLinkSource</a> and <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-cancellink">IOleUILinkContainer::CancelLink</a>. Your implementation of these methods can call <b>IOleLink::SetSourceDisplayName</b>.

If your container application is immediately going to bind to a newly specified link source, you should call <a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a> and <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setsourcemoniker">IOleLink::SetSourceMoniker</a> instead, and then call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource">IOleLink::BindToSource</a> using the bind context from the parsing operation. By reusing the bind context, you can avoid redundant loading of objects that might otherwise occur.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The contract for <b>IOleLink::SetSourceDisplayName</b> does not specify when the linked object will parse the display name into a moniker. The parsing can occur before <b>IOleLink::SetSourceDisplayName</b> returns, or the linked object can store the display name and parse it only when it needs to bind to the link source. Note that parsing the display name is potentially an expensive operation because it might require binding to the link source. The provided implementation of <b>IOleLink::SetSourceDisplayName</b> parses the display name and then releases the bind context used in the parse operation. This can result in running and then stopping the link source server.

If the linked object is bound to the current link source, the implementation of <b>IOleLink::SetSourceDisplayName</b> breaks the connection.

For more information on how the linked object stores and uses the moniker to the link source, see <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setsourcemoniker">IOleLink::SetSourceMoniker</a>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setsourcemoniker">IOleLink::SetSourceMoniker</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a>