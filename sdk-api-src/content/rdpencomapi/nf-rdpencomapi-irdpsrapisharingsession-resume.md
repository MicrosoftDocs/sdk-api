---
UID: NF:rdpencomapi.IRDPSRAPISharingSession.Resume
title: IRDPSRAPISharingSession::Resume (rdpencomapi.h)
description: Causes the graphics stream that is sent to all viewers from the sharer to resume until either IRDPSRAPISharingSession::Pause or IRDPSRAPISharingSession::Close is called.
helpviewer_keywords: ["IRDPSRAPISharingSession interface [RDP]","Resume method","IRDPSRAPISharingSession.Resume","IRDPSRAPISharingSession2 interface [RDP]","Resume method","IRDPSRAPISharingSession2::Resume","IRDPSRAPISharingSession::Resume","Resume","Resume method [RDP]","Resume method [RDP]","IRDPSRAPISharingSession interface","Resume method [RDP]","IRDPSRAPISharingSession2 interface","rdp.irdpsrapisharingsession_resume","rdpencomapi/IRDPSRAPISharingSession2::Resume","rdpencomapi/IRDPSRAPISharingSession::Resume"]
old-location: rdp\irdpsrapisharingsession_resume.htm
tech.root: rdp
ms.assetid: 3e99d514-a6fe-4855-99ab-9ab2b5cbcc9b
ms.date: 12/05/2018
ms.keywords: IRDPSRAPISharingSession interface [RDP],Resume method, IRDPSRAPISharingSession.Resume, IRDPSRAPISharingSession2 interface [RDP],Resume method, IRDPSRAPISharingSession2::Resume, IRDPSRAPISharingSession::Resume, Resume, Resume method [RDP], Resume method [RDP],IRDPSRAPISharingSession interface, Resume method [RDP],IRDPSRAPISharingSession2 interface, rdp.irdpsrapisharingsession_resume, rdpencomapi/IRDPSRAPISharingSession2::Resume, rdpencomapi/IRDPSRAPISharingSession::Resume
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - IRDPSRAPISharingSession::Resume
 - rdpencomapi/IRDPSRAPISharingSession::Resume
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
 - IRDPSRAPISharingSession2.Resume
 - IRDPSRAPISharingSession.Resume
---

# IRDPSRAPISharingSession::Resume


## -description

Causes the graphics stream that is sent to all viewers from the sharer to resume until either <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-pause">IRDPSRAPISharingSession::Pause</a> or <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-close">IRDPSRAPISharingSession::Close</a> is called.



## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession">IRDPSRAPISharingSession</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a>
