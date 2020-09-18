---
UID: NS:drt.drt_bootstrap_provider_tag
title: DRT_BOOTSTRAP_PROVIDER (drt.h)
description: DRT_BOOTSTRAP_PROVIDER structure defines the DRT interface that must be implemented by a bootstrap provider.
helpviewer_keywords: ["*PDRT_BOOTSTRAP_PROVIDER","DRT_BOOTSTRAP_PROVIDER","DRT_BOOTSTRAP_PROVIDER structure [Peer Networking]","PDRT_BOOTSTRAP_PROVIDER","PDRT_BOOTSTRAP_PROVIDER structure pointer [Peer Networking]","drt/DRT_BOOTSTRAP_PROVIDER","drt/PDRT_BOOTSTRAP_PROVIDER","p2p.drt_bootstrap_provider"]
old-location: p2p\drt_bootstrap_provider.htm
tech.root: p2p
ms.assetid: f64edf7f-379f-41e2-9a86-ba9aeee0f2d7
ms.date: 12/05/2018
ms.keywords: '*PDRT_BOOTSTRAP_PROVIDER, DRT_BOOTSTRAP_PROVIDER, DRT_BOOTSTRAP_PROVIDER structure [Peer Networking], PDRT_BOOTSTRAP_PROVIDER, PDRT_BOOTSTRAP_PROVIDER structure pointer [Peer Networking], drt/DRT_BOOTSTRAP_PROVIDER, drt/PDRT_BOOTSTRAP_PROVIDER, p2p.drt_bootstrap_provider'
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DRT_BOOTSTRAP_PROVIDER, *PDRT_BOOTSTRAP_PROVIDER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - drt_bootstrap_provider_tag
 - drt/drt_bootstrap_provider_tag
 - PDRT_BOOTSTRAP_PROVIDER
 - drt/PDRT_BOOTSTRAP_PROVIDER
 - DRT_BOOTSTRAP_PROVIDER
 - drt/DRT_BOOTSTRAP_PROVIDER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_BOOTSTRAP_PROVIDER
---

# DRT_BOOTSTRAP_PROVIDER structure


## -description

The <b>DRT_BOOTSTRAP_PROVIDER</b> structure defines the DRT interface that must be implemented by a bootstrap provider.
<div class="alert"><b>Note</b>  The DRT  infrastructure does not call the methods of the bootstrap provider concurrently.</div><div> </div>

## -struct-fields

### -field pvContext

Pointer to context data that is defined by the bootstrap resolver. When creating a bootstrap resolver, the developer  is required to populate the resolver with the required information; often times, this occurs as a "this" pointer.  This context gets passed to all the context parameters in the functions defined by the <b>DRT_BOOTSTRAP_PROVIDER</b>.

### -field Attach

Increments the count of references for the Bootstrap Provider with a set of DRTs.



#### pvContext

Contains the <b>pvContext</b> value from <b>DRT_BOOTSTRAP_PROVIDER</b>.

### -field Detach

Decrements the count of references for the Bootstrap Provider with a set of DRTs.



#### pvContext

Contains the <b>pvContext</b> value from <b>DRT_BOOTSTRAP_PROVIDER</b>.

### -field InitResolve

Called by the DRT infrastructure to supply configuration information about upcoming name resolutions.



#### pvContext

Contains the <b>pvContext</b> value from <b>DRT_BOOTSTRAP_PROVIDER</b>.



#### fSplitDetect

Specifies if the resolve operation is being utilized for network split detection and recovery.



#### timeout

Specifies the maximum time a resolve should take before timing out. This value is represented in milliseconds.



#### cMaxResults

Specifies the maximum number of results to return during the resolve operation.



#### ResolveContext

Pointer to resolver specific data.



#### fFatalError

If the bootstrap provider encounters an irrecoverable error, this parameter must be set to <b>TRUE</b> when the function complete in order for the DRT to transition to the faulted state. The <b>HRESULT</b> that is made available to the higher layer application for debugging will appear in the <b>hr</b> member of the <a href="/windows/desktop/api/drt/ns-drt-drt_event_data">DRT_EVENT_DATA</a> structure associated with the event signaling the transition to the faulted state.  This bootstrap provider function should not return S_OK if setting the <i>fFatalError</i> flag to <b>TRUE</b>.

### -field IssueResolve

Called by the DRT infrastructure to issue a resolution to determine the endpoints of nodes already active in the DRT cloud.



#### pvContext

Contains the <b>pvContext</b> value from <b>DRT_BOOTSTRAP_PROVIDER</b>.



#### pvCallbackContext

Pointer to the context data that is passed back to the callback defined by the next parameter.



#### callback

A BOOTSTRAP_RESOLVE_CALLBACK that is called back for each result and DRT_E_NO_MORE.



#### ResolveContext

Pointer to resolver specific data.



#### fFatalError

If the bootstrap provider encounters an irrecoverable error, this parameter must be set to <b>TRUE</b> when the function complete in order for the DRT to transition to the faulted state. The <b>HRESULT</b> that is made available to the higher layer application for debugging will appear in the <b>hr</b> member of the <a href="/windows/desktop/api/drt/ns-drt-drt_event_data">DRT_EVENT_DATA</a> structure associated with the event signaling the transition to the faulted state.  This bootstrap provider function should not return S_OK if setting the <i>fFatalError</i> flag to <b>TRUE</b>.

### -field EndResolve

Ends the resolution of an endpoint.



#### pvContext

Contains the <b>pvContext</b> value from <b>DRT_BOOTSTRAP_PROVIDER</b>.



#### ResolveContext

The <b>BOOTSTRAP_RESOLVE_CONTEXT</b> received from the Resolve function of the specified bootstrap provider.

### -field Register

Registers an endpoint with the bootstrapping mechanism. This process makes it possible for other nodes  find the endpoint via the bootstrap resolver.



#### pvContext

Contains the <b>pvContext</b> value from <b>DRT_BOOTSTRAP_PROVIDER</b>.



#### pAddressList

Pointer to the list of addresses to register with the bootstrapping mechanism.

### -field Unregister

This function deregisters an endpoint with the bootstrapping mechanism.  As a result, other nodes will be unable to find the local node via the bootstrap  resolver.



#### pvContext

Contains the <b>pvContext</b> value from <b>DRT_BOOTSTRAP_PROVIDER</b>.