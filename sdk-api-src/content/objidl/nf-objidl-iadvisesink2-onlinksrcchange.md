---
UID: NF:objidl.IAdviseSink2.OnLinkSrcChange
title: IAdviseSink2::OnLinkSrcChange (objidl.h)
description: Notifies the container that registered the advise sink that a link source has changed (either name or location), enabling the container to update the link's moniker.
helpviewer_keywords: ["IAdviseSink2 interface [COM]","OnLinkSrcChange method","IAdviseSink2.OnLinkSrcChange","IAdviseSink2::OnLinkSrcChange","OnLinkSrcChange","OnLinkSrcChange method [COM]","OnLinkSrcChange method [COM]","IAdviseSink2 interface","_ole_iadvisesink2_onlinksrcchange","com.iadvisesink2_onlinksrcchange","objidl/IAdviseSink2::OnLinkSrcChange"]
old-location: com\iadvisesink2_onlinksrcchange.htm
tech.root: com
ms.assetid: 753ac9a3-0207-4c98-9d86-5ac16be2c5fa
ms.date: 12/05/2018
ms.keywords: IAdviseSink2 interface [COM],OnLinkSrcChange method, IAdviseSink2.OnLinkSrcChange, IAdviseSink2::OnLinkSrcChange, OnLinkSrcChange, OnLinkSrcChange method [COM], OnLinkSrcChange method [COM],IAdviseSink2 interface, _ole_iadvisesink2_onlinksrcchange, com.iadvisesink2_onlinksrcchange, objidl/IAdviseSink2::OnLinkSrcChange
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IAdviseSink2::OnLinkSrcChange
 - objidl/IAdviseSink2::OnLinkSrcChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IAdviseSink2.OnLinkSrcChange
---

# IAdviseSink2::OnLinkSrcChange


## -description

Notifies the container that registered the advise sink that a link source has changed (either name or location), enabling the container to update the link's moniker.

## -parameters

### -param pmk [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface identifying the source of a linked object.

## -remarks

A container of linked objects implements this method to receive notification in the event of a change in the moniker of its link source.

<b>OnLinkSrcChange</b> is called by the OLE link object when it receives the <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onrename">OnRename</a> notification from the link-source (object) application. The link object updates its moniker and sends the <b>OnLinkSrcChange</b> notification to containers that have implemented <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink2">IAdviseSink2</a>.


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Nothing prevents a link object from notifying its container of the moniker change by calling <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onrename">OnRename</a> instead of <b>OnLinkSrcChange</b>. In practice, however, overloading <b>OnRename</b> to mean either that a link object's moniker has changed or that an embedded object's server name has changed makes it difficult for applications to determine which of these events has occurred. If the two events trigger different processing, as will often be the case, calling a different method for each makes the job of determining which event occurred much easier.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink2">IAdviseSink2</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onrename">IAdviseSink::OnRename</a>