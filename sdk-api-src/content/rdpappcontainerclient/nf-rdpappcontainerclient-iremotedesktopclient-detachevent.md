---
UID: NF:rdpappcontainerclient.IRemoteDesktopClient.detachEvent
title: IRemoteDesktopClient::detachEvent (rdpappcontainerclient.h)
description: Detaches an event handler from an event.
helpviewer_keywords: ["IRemoteDesktopClient interface [Remote Desktop Services]","detachEvent method","IRemoteDesktopClient.detachEvent","IRemoteDesktopClient::detachEvent","detachEvent","detachEvent method [Remote Desktop Services]","detachEvent method [Remote Desktop Services]","IRemoteDesktopClient interface","rdpappcontainerclient/IRemoteDesktopClient::detachEvent","termserv.iremotedesktopclient_detachevent"]
old-location: termserv\iremotedesktopclient_detachevent.htm
tech.root: TermServ
ms.assetid: 5913da44-3dc2-40a3-9808-3619e5fa91b4
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClient interface [Remote Desktop Services],detachEvent method, IRemoteDesktopClient.detachEvent, IRemoteDesktopClient::detachEvent, detachEvent, detachEvent method [Remote Desktop Services], detachEvent method [Remote Desktop Services],IRemoteDesktopClient interface, rdpappcontainerclient/IRemoteDesktopClient::detachEvent, termserv.iremotedesktopclient_detachevent
req.header: rdpappcontainerclient.h
req.include-header: 
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
 - IRemoteDesktopClient::detachEvent
 - rdpappcontainerclient/IRemoteDesktopClient::detachEvent
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
 - IRemoteDesktopClient.detachEvent
---

# IRemoteDesktopClient::detachEvent


## -description

Detaches an event handler from an event.

## -parameters

### -param eventName [in]

### -param callback [in]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient">IRemoteDesktopClient</a>