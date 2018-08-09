---
UID: NF:mspcall.CMSPCallBase.HandleStreamEvent
title: CMSPCallBase::HandleStreamEvent
author: windows-sdk-content
description: The HandleStreamEvent method is called by a stream to send an event to TAPI.
old-location: tapi3\cmspcallbase_handlestreamevent.htm
old-project: tapi
ms.assetid: 196f6b18-0de7-463b-9b0f-7b4d666e7470
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],HandleStreamEvent method, CMSPCallBase.HandleStreamEvent, CMSPCallBase::HandleStreamEvent, HandleStreamEvent, HandleStreamEvent method [TAPI 2.2], HandleStreamEvent method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_handlestreamevent, mspcall/CMSPCallBase::HandleStreamEvent, tapi3.cmspcallbase_handlestreamevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
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
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CMSPCallBase::HandleStreamEvent


## -description


The 
<b>HandleStreamEvent</b> method is called by a stream to send an event to TAPI. It fills in the call handle in the event info structure and then calls the PostEvent method on the MSP address object. (Note that this way, events generated on the streams "flow" toward the address object via the call object, with more information filled in at each step. This reduces the amount of state that must be kept in the MSP call and MSP stream objects.)


## -parameters




### -param EventItem

Pointer to 
<a href="https://msdn.microsoft.com/fc99fd05-4d87-4b6e-b2f3-e00ac61ddafc">MSPEVENTITEM</a>, a struct containing a linked list of 
<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>
 

 

