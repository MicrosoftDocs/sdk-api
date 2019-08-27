---
UID: NS:drt.drt_event_data_tag
title: DRT_EVENT_DATA (drt.h)
author: windows-sdk-content
description: DRT_EVENT_DATA.
old-location: p2p\drt_event_data.htm
tech.root: P2PSdk
ms.assetid: b52bf815-d962-4f72-8876-a80769bc3d3d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDRT_EVENT_DATA, DRT_EVENT_DATA, DRT_EVENT_DATA structure [Peer Networking], PDRT_EVENT_DATA, PDRT_EVENT_DATA structure pointer [Peer Networking], drt/DRT_EVENT_DATA, drt/PDRT_EVENT_DATA, p2p.drt_event_data"
ms.topic: struct
f1_keywords: 
 - "drt/DRT_EVENT_DATA"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_EVENT_DATA
product: Windows
targetos: Windows
req.typenames: DRT_EVENT_DATA, *PDRT_EVENT_DATA
req.redist: 
ms.custom: 19H1
---

# DRT_EVENT_DATA structure


## -description


The <b>DRT_EVENT_DATA</b> structure contains the event data returned by calling <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtgeteventdata">DrtGetEventData</a> after an application receives an event signal on the <i>hEvent</i> passed into <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>.


## -struct-fields




### -field type

A <a href="https://docs.microsoft.com/windows/desktop/api/drt/ne-drt-drt_event_type">DRT_EVENT_TYPE</a> enumeration that specifies the event type.


### -field hr

The HRESULT of the operation for which the event was signaled that indicates if a result is the last result within a search.


### -field pvContext

Pointer to the context data passed to the API that generated the event.  For example, if data is passed into the <i>pvContext</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>, that data is returned through this field.


### -field leafsetKeyChange

 


### -field leafsetKeyChange.change

 


### -field leafsetKeyChange.localKey

 


### -field leafsetKeyChange.remoteKey

 


### -field registrationStateChange

 


### -field registrationStateChange.state

 


### -field registrationStateChange.localKey

 


### -field statusChange

 


### -field statusChange.status

 


### -field statusChange.bootstrapAddresses

 


### -field statusChange.bootstrapAddresses.cntAddress

 


### -field statusChange.bootstrapAddresses.pAddresses

 




#### - ( unnamed union )

Union that contains a structure that defines a change in the leaf set, the state of a locally registered key, or the state of the local DRT instance.



#### leafsetKeyChange

This structure appears when the event has been raised to signal a change in a leaf set of a locally registered key; the <b>type</b> field of the <b>DRT_EVENT_DATA</b> structure is set to DRT_EVENT_LEAFSET_KEY_CHANGED.



##### change

Specifies the type of key change that has occurred.



##### localKey

Specifies the local key associated with the leaf set that has changed.



##### remoteKey

Specifies the remote key that changed.



#### registrationStateChange

This structure appears when the event has been raised to signal a change in a local key registration; the <b>type</b>  field of the <b>DRT_EVENT_DATA</b> structure is set to DRT_EVENT_REGISTRATION_STATE_CHANGED.



##### state

Specifies the type of registration state change that has occurred.



##### localKey

Specifies the local key associated with the registration that has changed.



#### statusChange

This structure appears when the event has been raised to signal a state change in the local DRT instance; the <b>type</b> field of the <b>DRT_EVENT_DATA</b> structure is set to DRT_EVENT_STATUS_CHANGED.



##### status

Contains the current <a href="https://docs.microsoft.com/windows/desktop/api/drt/ne-drt-drt_status">DRT_STATUS</a> of the  local DRT instance.



##### bootstrapAddresses

This structure contains the addresses returned by the bootstrap provider when the DRT attempts to join the mesh. This structure is completed only when the DRT transitions to the DRT_ALONE state. The contents of this structure can be used to diagnose connectivity issues between the local DRT instance and other nodes already present in the mesh.



###### cntAddress

Contains the number of addresses in <b>pAddresses</b>.



###### pAddresses

Contains an array of addresses returned by the bootstrap provider.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/ne-drt-drt_event_type">DRT_EVENT_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/ne-drt-drt_status">DRT_STATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtgeteventdata">DrtGetEventData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>
 

 

