---
UID: NF:rdpappcontainerclient.IRemoteDesktopClient.attachEvent
title: IRemoteDesktopClient::attachEvent (rdpappcontainerclient.h)
description: Attaches an event handler to an event.
helpviewer_keywords: ["IRemoteDesktopClient interface [Remote Desktop Services]","attachEvent method","IRemoteDesktopClient.attachEvent","IRemoteDesktopClient::attachEvent","attachEvent","attachEvent method [Remote Desktop Services]","attachEvent method [Remote Desktop Services]","IRemoteDesktopClient interface","rdpappcontainerclient/IRemoteDesktopClient::attachEvent","termserv.iremotedesktopclient_attachevent"]
old-location: termserv\iremotedesktopclient_attachevent.htm
tech.root: TermServ
ms.assetid: a904827b-644b-459b-b1bd-399bad21f94f
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClient interface [Remote Desktop Services],attachEvent method, IRemoteDesktopClient.attachEvent, IRemoteDesktopClient::attachEvent, attachEvent, attachEvent method [Remote Desktop Services], attachEvent method [Remote Desktop Services],IRemoteDesktopClient interface, rdpappcontainerclient/IRemoteDesktopClient::attachEvent, termserv.iremotedesktopclient_attachevent
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
 - IRemoteDesktopClient::attachEvent
 - rdpappcontainerclient/IRemoteDesktopClient::attachEvent
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
 - IRemoteDesktopClient.attachEvent
---

# IRemoteDesktopClient::attachEvent


## -description

Attaches an event handler to an event.

## -parameters

### -param eventName [in]

### -param callback [in]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient">IRemoteDesktopClient</a>