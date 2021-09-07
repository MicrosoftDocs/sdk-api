---
UID: NN:rdpencomapi.IRDPSRAPIAttendee
title: IRDPSRAPIAttendee (rdpencomapi.h)
description: Attendee objects are created as a result of clients connecting to the session and being authenticated. After an attendee object is created, it is automatically added to the attendees list.
helpviewer_keywords: ["IRDPSRAPIAttendee","IRDPSRAPIAttendee interface [RDP]","IRDPSRAPIAttendee interface [RDP]","described","rdp.irdpsrapiattendee","rdpencomapi/IRDPSRAPIAttendee"]
old-location: rdp\irdpsrapiattendee.htm
tech.root: rdp
ms.assetid: e9edd9f2-ccbf-45b2-b71c-e30368435a60
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIAttendee, IRDPSRAPIAttendee interface [RDP], IRDPSRAPIAttendee interface [RDP],described, rdp.irdpsrapiattendee, rdpencomapi/IRDPSRAPIAttendee
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
 - IRDPSRAPIAttendee
 - rdpencomapi/IRDPSRAPIAttendee
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
 - IRDPSRAPIAttendee
---

# IRDPSRAPIAttendee interface


## -description

Attendee objects are created as a result of clients connecting to the session and being authenticated. After an attendee object is created, it is automatically added to the attendees list.You cannot create an instance of this object. Applications can get access to attendee objects in the following ways:

<ul>
<li>When the <a href="/previous-versions/windows/desktop/rdp/onattendeeconnected">IRDPSessionEvents::OnAttendeeConnected</a> event is fired, the parameter is an <b>IDispatch</b> pointer corresponding to the attendee object that was created.</li>
<li>By accessing the Attendee property of the AttendeeDisconnectInfo object. An <b>IDispatch</b> pointer to this object is fired by the <a href="/previous-versions/windows/desktop/rdp/onattendeedisconnected">IRDPSessionEvents::OnAttendeeDisconnected</a> event. This is how applications are informed of what attendee was disconnected.</li>
<li>By calling the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiattendeemanager-get_item">get_Item</a> method on the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiattendeemanager">IRDPSRAPIAttendeeManager</a> interface.</li>
<li>By calling <b>get_Next</b> on the enumerator returned by the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiattendeemanager-get__newenum">IRDPSRAPIAttendeeManager::get__NewEnum</a> method.</li>
</ul>

## -inheritance

The <b>IRDPSRAPIAttendee</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRDPSRAPIAttendee</b> also has these types of members:

## -remarks

Applications should not save pointers to attendee objects. The lifetime of the attendee object depends on the lifetime of the <b>RDPSession</b> object. It also depends if the session is still in the opened state and if the client corresponding to the attendee object is still connected to the session. Applications can keep references to attendee objects but calling some methods on it after the client disconnected or after the session is destroyed will return <b>E_UNEXPECTED</b> failures.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiattendeedisconnectinfo">IRDPSRAPIAttendeeDisconnectInfo</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiattendeemanager">IRDPSRAPIAttendeeManager</a>
