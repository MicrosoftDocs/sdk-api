---
UID: NN:rdpencomapi.IRDPSRAPISharingSession
title: IRDPSRAPISharingSession (rdpencomapi.h)
description: The main object that an application must create to start a collaboration session. (IRDPSRAPISharingSession)
helpviewer_keywords: ["IRDPSRAPISharingSession","IRDPSRAPISharingSession interface [RDP]","IRDPSRAPISharingSession interface [RDP]","described","rdp.irdpsrapisharingsession","rdpencomapi/IRDPSRAPISharingSession"]
old-location: rdp\irdpsrapisharingsession.htm
tech.root: rdp
ms.assetid: 531382ec-d94f-411e-bd43-86cd3066ac26
ms.date: 12/05/2018
ms.keywords: IRDPSRAPISharingSession, IRDPSRAPISharingSession interface [RDP], IRDPSRAPISharingSession interface [RDP],described, rdp.irdpsrapisharingsession, rdpencomapi/IRDPSRAPISharingSession
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IRDPSRAPISharingSession
 - rdpencomapi/IRDPSRAPISharingSession
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
 - IRDPSRAPISharingSession
---

# IRDPSRAPISharingSession interface


## -description

The main object that an application must create  to start a collaboration session. It is also the only object that you can create an instance of. The rest of the objects are accessed as session object properties.

The session object is hosted in-process by RdpEncom.dll. Even if the object is hosted in-process, there can be only one instance of this object created within a Winlogon session. Creating a second object will fail.

This interface uses the  single-threaded apartment (STA) threading model.
The object exposes a source interface that is used for firing session-specific events (<a href="/windows/win32/api/rdpencomapi/nn-rdpencomapi-_irdpsessionevents">_IRDPSessionEvents</a>) and a dual interface that is used for managing a session.

## -inheritance

The <b>IRDPSRAPISharingSession</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRDPSRAPISharingSession</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a>
