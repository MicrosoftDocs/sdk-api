---
UID: NF:rdpencomapi.IRDPViewerInputSink.AddTouchInput
title: IRDPViewerInputSink::AddTouchInput (rdpencomapi.h)
description: Accepts a description of a touch input.
helpviewer_keywords: ["AddTouchInput","AddTouchInput method [RDP]","AddTouchInput method [RDP]","IRDPViewerInputSink interface","IRDPViewerInputSink interface [RDP]","AddTouchInput method","IRDPViewerInputSink.AddTouchInput","IRDPViewerInputSink::AddTouchInput","rdp.irdpviewerinputsink_addtouchinput","rdpencomapi/IRDPViewerInputSink::AddTouchInput"]
old-location: rdp\irdpviewerinputsink_addtouchinput.htm
tech.root: rdp
ms.assetid: 5DD220B8-505E-43AE-9438-F1D553AABB0B
ms.date: 12/05/2018
ms.keywords: AddTouchInput, AddTouchInput method [RDP], AddTouchInput method [RDP],IRDPViewerInputSink interface, IRDPViewerInputSink interface [RDP],AddTouchInput method, IRDPViewerInputSink.AddTouchInput, IRDPViewerInputSink::AddTouchInput, rdp.irdpviewerinputsink_addtouchinput, rdpencomapi/IRDPViewerInputSink::AddTouchInput
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPViewerInputSink::AddTouchInput
 - rdpencomapi/IRDPViewerInputSink::AddTouchInput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPViewerInputSink.AddTouchInput
---

# IRDPViewerInputSink::AddTouchInput


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpviewerinputsink">IRDPViewerInputSink</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Accepts a description of  a touch input.

## -parameters

### -param contactId

The identifier of the contact that generated the touch input.

### -param event

The event that results from the input.

### -param x

The touch position in the x-axis.

### -param y

The touch position in the y-axis.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerinputsink-begintouchframe">BeginTouchFrame</a>



<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerinputsink-endtouchframe">EndTouchFrame</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpviewerinputsink">IRDPViewerInputSink</a>