---
UID: NF:rdpappcontainerclient.IRemoteDesktopClientTouchPointer.put_EventsEnabled
title: IRemoteDesktopClientTouchPointer::put_EventsEnabled (rdpappcontainerclient.h)
description: Whether touch pointer event notifications are enabled for the RDP app container client control. (Put)
helpviewer_keywords: ["EventsEnabled property [Remote Desktop Services]","EventsEnabled property [Remote Desktop Services]","IRemoteDesktopClientTouchPointer interface","IRemoteDesktopClientTouchPointer interface [Remote Desktop Services]","EventsEnabled property","IRemoteDesktopClientTouchPointer.EventsEnabled","IRemoteDesktopClientTouchPointer.put_EventsEnabled","IRemoteDesktopClientTouchPointer::EventsEnabled","IRemoteDesktopClientTouchPointer::get_EventsEnabled","IRemoteDesktopClientTouchPointer::put_EventsEnabled","put_EventsEnabled","rdpappcontainerclient/IRemoteDesktopClientTouchPointer::EventsEnabled","rdpappcontainerclient/IRemoteDesktopClientTouchPointer::get_EventsEnabled","rdpappcontainerclient/IRemoteDesktopClientTouchPointer::put_EventsEnabled","termserv.iremotedesktopclienttouchpointer_eventsenabled"]
old-location: termserv\iremotedesktopclienttouchpointer_eventsenabled.htm
tech.root: TermServ
ms.assetid: 972e0f05-74fb-4997-a1c2-90ecfa4870a3
ms.date: 12/05/2018
ms.keywords: EventsEnabled property [Remote Desktop Services], EventsEnabled property [Remote Desktop Services],IRemoteDesktopClientTouchPointer interface, IRemoteDesktopClientTouchPointer interface [Remote Desktop Services],EventsEnabled property, IRemoteDesktopClientTouchPointer.EventsEnabled, IRemoteDesktopClientTouchPointer.put_EventsEnabled, IRemoteDesktopClientTouchPointer::EventsEnabled, IRemoteDesktopClientTouchPointer::get_EventsEnabled, IRemoteDesktopClientTouchPointer::put_EventsEnabled, put_EventsEnabled, rdpappcontainerclient/IRemoteDesktopClientTouchPointer::EventsEnabled, rdpappcontainerclient/IRemoteDesktopClientTouchPointer::get_EventsEnabled, rdpappcontainerclient/IRemoteDesktopClientTouchPointer::put_EventsEnabled, termserv.iremotedesktopclienttouchpointer_eventsenabled
req.header: rdpappcontainerclient.h
req.include-header: Rdpappcontainerclient.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsTscAx.dll
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRemoteDesktopClientTouchPointer::put_EventsEnabled
 - rdpappcontainerclient/IRemoteDesktopClientTouchPointer::put_EventsEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsTscAx.dll
api_name:
 - IRemoteDesktopClientTouchPointer.EventsEnabled
 - IRemoteDesktopClientTouchPointer.get_EventsEnabled
 - IRemoteDesktopClientTouchPointer.put_EventsEnabled
---

# IRemoteDesktopClientTouchPointer::put_EventsEnabled


## -description

Whether touch pointer event notifications are enabled for the RDP app container client control. If this property is enabled, the <a href="/windows/desktop/TermServ/iremotedesktopclientevents-ontouchpointercursormoved">OnTouchPointerCursorMoved</a> method will handle events when the touch pointer cursor is moved.

This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer">IRemoteDesktopClientTouchPointer</a>
