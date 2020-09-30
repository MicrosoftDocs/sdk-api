---
UID: NF:upnp.IUPnPDescriptionDocument.get_ReadyState
title: IUPnPDescriptionDocument::get_ReadyState (upnp.h)
description: The ReadyState property specifies the status of the document load operation.
helpviewer_keywords: ["IUPnPDescriptionDocument interface [UPnP APIs]","get_ReadyState method","IUPnPDescriptionDocument.get_ReadyState","IUPnPDescriptionDocument::get_ReadyState","READYSTATE _COMPLETE","READYSTATE _INTERACTIVE","READYSTATE _LOADED","READYSTATE _LOADING","READYSTATE_UNINITIALIZED","_upnp_iupnpdescriptiondocument_readystate","get_ReadyState","get_ReadyState method [UPnP APIs]","get_ReadyState method [UPnP APIs]","IUPnPDescriptionDocument interface","upnp.iupnpdescriptiondocument_readystate","upnp/IUPnPDescriptionDocument::get_ReadyState"]
old-location: upnp\iupnpdescriptiondocument_readystate.htm
tech.root: upnp
ms.assetid: 592939fa-ebce-419f-a813-ecbbe788fd8e
ms.date: 12/05/2018
ms.keywords: IUPnPDescriptionDocument interface [UPnP APIs],get_ReadyState method, IUPnPDescriptionDocument.get_ReadyState, IUPnPDescriptionDocument::get_ReadyState, READYSTATE _COMPLETE, READYSTATE _INTERACTIVE, READYSTATE _LOADED, READYSTATE _LOADING, READYSTATE_UNINITIALIZED, _upnp_iupnpdescriptiondocument_readystate, get_ReadyState, get_ReadyState method [UPnP APIs], get_ReadyState method [UPnP APIs],IUPnPDescriptionDocument interface, upnp.iupnpdescriptiondocument_readystate, upnp/IUPnPDescriptionDocument::get_ReadyState
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Upnp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPDescriptionDocument::get_ReadyState
 - upnp/IUPnPDescriptionDocument::get_ReadyState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDescriptionDocument.get_ReadyState
---

# IUPnPDescriptionDocument::get_ReadyState


## -description

The 
<b>ReadyState</b> property specifies the status of the document load operation. This status indicates the state of the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-load">IUPnPDescriptionDocument::Load</a> or <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-loadasync">IUPnPDescriptionDocument::LoadAsync</a> method. These states are the standard ready-state values for loading XML documents.

## -parameters

### -param plReadyState [out]

Receives a reference to the ready state. The values this parameter can receive are (in the order they are used by Universal Plug and Play): 



<table>
<tr>
<th>plReadyState Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="READYSTATE_UNINITIALIZED"></a><a id="readystate_uninitialized"></a><dl>
<dt><b>READYSTATE_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The document object has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="READYSTATE__LOADING"></a><a id="readystate__loading"></a><dl>
<dt><b>READYSTATE _LOADING</b></dt>
</dl>
</td>
<td width="60%">
The load operation has started.

</td>
</tr>
<tr>
<td width="40%"><a id="READYSTATE__COMPLETE"></a><a id="readystate__complete"></a><dl>
<dt><b>READYSTATE _COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The load operation is finished; the document has been downloaded and the XML has been parsed.

</td>
</tr>
<tr>
<td width="40%"><a id="READYSTATE__INTERACTIVE"></a><a id="readystate__interactive"></a><dl>
<dt><b>READYSTATE _INTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="READYSTATE__LOADED"></a><a id="readystate__loaded"></a><dl>
<dt><b>READYSTATE _LOADED</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
</table>

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocument">IUPnPDescriptionDocument</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-load">IUPnPDescriptionDocument::Load</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-loadasync">IUPnPDescriptionDocument::LoadAsync</a>