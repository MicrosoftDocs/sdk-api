---
UID: NN:rdpencomapi.IRDPSRAPIFrameBuffer
title: IRDPSRAPIFrameBuffer (rdpencomapi.h)
description: Provides data about the frame buffer size and format and allows the contents to be retrieved.
helpviewer_keywords: ["IRDPSRAPIFrameBuffer","IRDPSRAPIFrameBuffer interface [RDP]","IRDPSRAPIFrameBuffer interface [RDP]","described","rdp.irdpsrapiframebuffer","rdpencomapi/IRDPSRAPIFrameBuffer"]
old-location: rdp\irdpsrapiframebuffer.htm
tech.root: rdp
ms.assetid: ab40bdd2-448f-4867-aabd-d6b66add5247
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIFrameBuffer, IRDPSRAPIFrameBuffer interface [RDP], IRDPSRAPIFrameBuffer interface [RDP],described, rdp.irdpsrapiframebuffer, rdpencomapi/IRDPSRAPIFrameBuffer
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - IRDPSRAPIFrameBuffer
 - rdpencomapi/IRDPSRAPIFrameBuffer
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
 - IRDPSRAPIFrameBuffer
---

# IRDPSRAPIFrameBuffer interface


## -description

Provides data about the frame buffer size and format and allows the contents to be retrieved.

Applications can get a pointer to this interface from the <b>FrameBuffer</b> property of the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a> interface.

## -inheritance

The <b>IRDPSRAPIFrameBuffer</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRDPSRAPIFrameBuffer</b> also has these types of members:

