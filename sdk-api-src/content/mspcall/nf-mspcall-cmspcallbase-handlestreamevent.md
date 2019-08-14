---
UID: NF:mspcall.CMSPCallBase.HandleStreamEvent
title: CMSPCallBase::HandleStreamEvent (mspcall.h)
author: windows-sdk-content
description: The HandleStreamEvent method is called by a stream to send an event to TAPI.
old-location: tapi3\cmspcallbase_handlestreamevent.htm
tech.root: Tapi
ms.assetid: 196f6b18-0de7-463b-9b0f-7b4d666e7470
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],HandleStreamEvent method, CMSPCallBase.HandleStreamEvent, CMSPCallBase::HandleStreamEvent, HandleStreamEvent, HandleStreamEvent method [TAPI 2.2], HandleStreamEvent method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_handlestreamevent, mspcall/CMSPCallBase::HandleStreamEvent, tapi3.cmspcallbase_handlestreamevent
ms.topic: method
f1_keywords: 
 - "mspcall/CMSPCallBase.HandleStreamEvent"
req.header: mspcall.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallBase.HandleStreamEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CMSPCallBase::HandleStreamEvent


## -description


The 
<b>HandleStreamEvent</b> method is called by a stream to send an event to TAPI. It fills in the call handle in the event info structure and then calls the PostEvent method on the MSP address object. (Note that this way, events generated on the streams "flow" toward the address object via the call object, with more information filled in at each step. This reduces the amount of state that must be kept in the MSP call and MSP stream objects.)


## -parameters




### -param EventItem

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/mspaddr/ns-mspaddr-mspeventitem">MSPEVENTITEM</a>, a struct containing a linked list of 
<a href="https://docs.microsoft.com/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a> structures.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nl-mspcall-cmspcallbase">CMSPCallBase</a>
 

 

