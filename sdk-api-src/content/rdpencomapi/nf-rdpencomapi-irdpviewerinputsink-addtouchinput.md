---
UID: NF:rdpencomapi.IRDPViewerInputSink.AddTouchInput
title: IRDPViewerInputSink::AddTouchInput
author: windows-sdk-content
description: Accepts a description of a touch input.
old-location: rdp\irdpviewerinputsink_addtouchinput.htm
tech.root: Rdp
ms.assetid: 5DD220B8-505E-43AE-9438-F1D553AABB0B
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddTouchInput, AddTouchInput method [RDP], AddTouchInput method [RDP],IRDPViewerInputSink interface, IRDPViewerInputSink interface [RDP],AddTouchInput method, IRDPViewerInputSink.AddTouchInput, IRDPViewerInputSink::AddTouchInput, rdp.irdpviewerinputsink_addtouchinput, rdpencomapi/IRDPViewerInputSink::AddTouchInput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPViewerInputSink.AddTouchInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPViewerInputSink::AddTouchInput


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/364EC709-C41C-4ADD-8E7D-6A635E5BCCDA">IRDPViewerInputSink</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

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




<a href="https://msdn.microsoft.com/DCB67D63-A866-4D98-907B-6CDB7EB56312">BeginTouchFrame</a>



<a href="https://msdn.microsoft.com/31E84AEB-7A89-4EF1-9744-3102AAEA2C1E">EndTouchFrame</a>



<a href="https://msdn.microsoft.com/364EC709-C41C-4ADD-8E7D-6A635E5BCCDA">IRDPViewerInputSink</a>
 

 

