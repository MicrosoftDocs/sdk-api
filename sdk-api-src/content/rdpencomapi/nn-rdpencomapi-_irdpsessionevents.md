---
UID: NN:rdpencomapi._IRDPSessionEvents
title: _IRDPSessionEvents (rdpencomapi.h)
description: Implement this interface to receive notifications when events occur.
helpviewer_keywords: ["_IRDPSessionEvents","_IRDPSessionEvents interface [RDP]","_IRDPSessionEvents interface [RDP]","described","rdp._irdpsessionevents","rdpencomapi/_IRDPSessionEvents"]
old-location: rdp\_irdpsessionevents.htm
tech.root: rdp
ms.assetid: 89ffdf37-156f-4977-93c4-bf9fe5aec838
ms.date: 12/05/2018
ms.keywords: _IRDPSessionEvents, _IRDPSessionEvents interface [RDP], _IRDPSessionEvents interface [RDP],described, rdp._irdpsessionevents, rdpencomapi/_IRDPSessionEvents
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
 - _IRDPSessionEvents
 - rdpencomapi/_IRDPSessionEvents
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
 - _IRDPSessionEvents
---

# _IRDPSessionEvents interface


## -description

Implement this interface to receive notifications when events occur.

## -remarks

The RDPViewer COM object is a connectable object. To receive events from the object about the connection sharing session, an application can implement **_IRdpSessionEvents** and perform the following steps.

1. Call [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) on the RDPViewer to obtain a pointer to the [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface.
1. Call [IConnectionPointContainer::FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint), specifying `__uuidof(_IRdpSessionEvents)` as the *riid* parameter, to obtain a pointer to the [IConnectionPoint](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) interface of the client control events. 
1. Call [IConnectionPoint::Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) to specify the calling application's own implementation of **_IRdpSessionEvents** where the events are to be dispatched. 

Application can use the following DISPIDs when implementing **IDispatch::Invoke**.

| dispIdMember | Dispatch to method |
|--------------|--------------------|
| DISPID_RDPSRAPI_EVENT_ON_ATTENDEE_CONNECTED = 301| [OnAttendeeConnected](/previous-versions/windows/desktop/rdp/onattendeeconnected) |
| DISPID_RDPSRAPI_EVENT_ON_ATTENDEE_DISCONNECTED = 302| [OnAttendeeDisconnected](/previous-versions/windows/desktop/rdp/onattendeedisconnected) |
| DISPID_RDPSRAPI_EVENT_ON_ATTENDEE_UPDATE = 303| [OnAttendeeUpdate](/previous-versions/windows/desktop/rdp/onattendeeupdate) |
| DISPID_RDPSRAPI_EVENT_ON_ERROR = 304| [OnError](/previous-versions/windows/desktop/rdp/onerror) |
| DISPID_RDPSRAPI_EVENT_ON_APPLICATION_OPEN = 316| [OnApplicationOpen](/previous-versions/windows/desktop/rdp/onapplicationopen) |
| DISPID_RDPSRAPI_EVENT_ON_APPLICATION_CLOSE = 317| [OnApplicationClose](/previous-versions/windows/desktop/rdp/onapplicationclose) |
| DISPID_RDPSRAPI_EVENT_ON_APPLICATION_UPDATE = 318| [OnApplicationUpdate](/previous-versions/windows/desktop/rdp/onapplicationupdate) |
| DISPID_RDPSRAPI_EVENT_ON_WINDOW_OPEN = 319 | [OnWindowOpen](/previous-versions/windows/desktop/rdp/onwindowopen) |
| DISPID_RDPSRAPI_EVENT_ON_WINDOW_CLOSE = 320 | | [OnWindowClose](/previous-versions/windows/desktop/rdp/onwindowclose) |
| DISPID_RDPSRAPI_EVENT_ON_WINDOW_UPDATE = 321 | [OnWindowUpdate](/previous-versions/windows/desktop/rdp/onwindowupdate) |
| DISPID_RDPSRAPI_EVENT_ON_CTRLLEVEL_CHANGE_REQUEST = 309 | [OnControlLevelChangeRequest](/previous-versions/windows/desktop/rdp/oncontrollevelchangerequest) |
| DISPID_RDPSRAPI_EVENT_ON_VIEWER_CONNECTED = 305 | [OnConnectionEstablished](/previous-versions/windows/desktop/rdp/onconnectionestablished) |
| DISPID_RDPSRAPI_EVENT_ON_VIEWER_CONNECTFAILED = 308 | [OnConnectionFailed](/previous-versions/windows/desktop/rdp/onconnectionfailed) |
| DISPID_RDPSRAPI_EVENT_ON_VIEWER_AUTHENTICATED = 307 | [OnConnectionAuthenticated](/previous-versions/windows/desktop/rdp/onconnectionauthenticated) |
| DISPID_RDPSRAPI_EVENT_ON_VIEWER_DISCONNECTED = 306 | [OnConnectionTerminated](/previous-versions/windows/desktop/rdp/onconnectionterminated) |
| DISPID_RDPSRAPI_EVENT_ON_APPFILTER_UPDATE = 322 | None. A notification that the application filter returned by IRDPSRAPISharingSession::get_ApplicationFilter has changed.
| DISPID_RDPSRAPI_EVENT_ON_GRAPHICS_STREAM_PAUSED = 310 | [OnGraphicsStreamPaused](/previous-versions/windows/desktop/rdp/ongraphicsstreampaused) |
| DISPID_RDPSRAPI_EVENT_ON_GRAPHICS_STREAM_RESUMED = 311 | [OnGraphicsStreamResumed](/previous-versions/windows/desktop/rdp/ongraphicsstreamresumed) |
| DISPID_RDPSRAPI_EVENT_ON_VIRTUAL_CHANNEL_DATARECEIVED = 314 | [OnChannelDataReceived](/previous-versions/windows/desktop/rdp/onchanneldatareceived) |
| DISPID_RDPSRAPI_EVENT_ON_VIRTUAL_CHANNEL_SENDCOMPLETED = 315 | [OnChannelDataSent](/previous-versions/windows/desktop/rdp/onchanneldatasent) |
| DISPID_RDPSRAPI_EVENT_ON_SHARED_RECT_CHANGED = 323 | [OnSharedRectChanged](/previous-versions/windows/desktop/rdp/onsharedrectchanged) |
| DISPID_RDPSRAPI_EVENT_ON_FOCUSRELEASED = 324 | [OnFocusReleased](/previous-versions/windows/desktop/rdp/onfocusreleased) |
| DISPID_RDPSRAPI_EVENT_ON_SHARED_DESKTOP_SETTINGS_CHANGED = 325 | [OnSharedDesktopSettingsChanged](/previous-versions/windows/desktop/rdp/onshareddesktopsettingschanged) |
| DISPID_RDPAPI_EVENT_ON_BOUNDING_RECT_CHANGED = 340 | [OnViewingSizeChanged](/previous-versions/windows/desktop/legacy/hh802749(v=vs.85)) |


## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>