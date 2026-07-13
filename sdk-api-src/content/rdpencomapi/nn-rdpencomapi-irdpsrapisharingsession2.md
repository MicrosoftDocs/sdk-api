---
UID: NN:rdpencomapi.IRDPSRAPISharingSession2
title: IRDPSRAPISharingSession2 (rdpencomapi.h)
description: The main object that an application must create to start a collaboration session. (IRDPSRAPISharingSession2)
helpviewer_keywords: ["IRDPSRAPISharingSession2","IRDPSRAPISharingSession2 interface [RDP]","IRDPSRAPISharingSession2 interface [RDP]","described","rdp.irdpsrapisharingsession2","rdpencomapi/IRDPSRAPISharingSession2"]
old-location: rdp\irdpsrapisharingsession2.htm
tech.root: rdp
ms.assetid: 3ac68be7-e6fd-42c7-b2f3-b90bb5097b07
ms.date: 12/05/2018
ms.keywords: IRDPSRAPISharingSession2, IRDPSRAPISharingSession2 interface [RDP], IRDPSRAPISharingSession2 interface [RDP],described, rdp.irdpsrapisharingsession2, rdpencomapi/IRDPSRAPISharingSession2
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
 - IRDPSRAPISharingSession2
 - rdpencomapi/IRDPSRAPISharingSession2
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
 - IRDPSRAPISharingSession2
---

# IRDPSRAPISharingSession2 interface


## -description

The main object that an application must create  to start a collaboration session. The 
    session object is hosted in-process by RdpEncom.dll. Even though session object is hosted in-process, 
    there can be only one instance of this object created within a Winlogon session. Creating a second object will 
    fail.

This interface uses the  single-threaded apartment (STA) threading model. The object exposes a source interface 
    that is used for firing session-specific events 
    (<a href="/windows/win32/api/rdpencomapi/nn-rdpencomapi-_irdpsessionevents">_IRDPSessionEvents</a>) and a dual interface that is used 
    for managing a session.

This interface extends the 
    <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession">IRDPSRAPISharingSession</a> interface and contains the 
    following members.

## -inheritance

The <b>IRDPSRAPISharingSession2</b> interface inherits from <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession">IRDPSRAPISharingSession</a>. <b>IRDPSRAPISharingSession2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession">IRDPSRAPISharingSession</a>
