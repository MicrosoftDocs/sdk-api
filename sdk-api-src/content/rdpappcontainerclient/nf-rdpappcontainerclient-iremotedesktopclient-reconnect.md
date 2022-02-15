---
UID: NF:rdpappcontainerclient.IRemoteDesktopClient.Reconnect
title: IRemoteDesktopClient::Reconnect (rdpappcontainerclient.h)
description: Initiates an automatic reconnection of the Remote Desktop Protocol (RDP) app container client control to fit the session to the new width and height.
helpviewer_keywords: ["IRemoteDesktopClient interface [Remote Desktop Services]","Reconnect method","IRemoteDesktopClient.Reconnect","IRemoteDesktopClient::Reconnect","Reconnect","Reconnect method [Remote Desktop Services]","Reconnect method [Remote Desktop Services]","IRemoteDesktopClient interface","rdpappcontainerclient/IRemoteDesktopClient::Reconnect","termserv.iremotedesktopclient_reconnect"]
old-location: termserv\iremotedesktopclient_reconnect.htm
tech.root: TermServ
ms.assetid: ef000769-a2d8-4d62-99d9-33ffc18ec8f6
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClient interface [Remote Desktop Services],Reconnect method, IRemoteDesktopClient.Reconnect, IRemoteDesktopClient::Reconnect, Reconnect, Reconnect method [Remote Desktop Services], Reconnect method [Remote Desktop Services],IRemoteDesktopClient interface, rdpappcontainerclient/IRemoteDesktopClient::Reconnect, termserv.iremotedesktopclient_reconnect
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
 - IRemoteDesktopClient::Reconnect
 - rdpappcontainerclient/IRemoteDesktopClient::Reconnect
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
 - IRemoteDesktopClient.Reconnect
---

# IRemoteDesktopClient::Reconnect


## -description

Initiates an automatic reconnection of the Remote Desktop Protocol (RDP) app container client control to fit the session to the new width and height.

## -parameters

### -param width [in]

### -param height [in]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient">IRemoteDesktopClient</a>