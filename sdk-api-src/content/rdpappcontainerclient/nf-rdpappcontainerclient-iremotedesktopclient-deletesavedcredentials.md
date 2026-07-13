---
UID: NF:rdpappcontainerclient.IRemoteDesktopClient.DeleteSavedCredentials
title: IRemoteDesktopClient::DeleteSavedCredentials (rdpappcontainerclient.h)
description: Deletes saved credentials for the specified remote computer.
helpviewer_keywords: ["DeleteSavedCredentials","DeleteSavedCredentials method [Remote Desktop Services]","DeleteSavedCredentials method [Remote Desktop Services]","IRemoteDesktopClient interface","IRemoteDesktopClient interface [Remote Desktop Services]","DeleteSavedCredentials method","IRemoteDesktopClient.DeleteSavedCredentials","IRemoteDesktopClient::DeleteSavedCredentials","rdpappcontainerclient/IRemoteDesktopClient::DeleteSavedCredentials","termserv.iremotedesktopclient_deletesavedcredentials"]
old-location: termserv\iremotedesktopclient_deletesavedcredentials.htm
tech.root: TermServ
ms.assetid: 9addc8de-1e82-47a3-a10e-566bacc3e37c
ms.date: 12/05/2018
ms.keywords: DeleteSavedCredentials, DeleteSavedCredentials method [Remote Desktop Services], DeleteSavedCredentials method [Remote Desktop Services],IRemoteDesktopClient interface, IRemoteDesktopClient interface [Remote Desktop Services],DeleteSavedCredentials method, IRemoteDesktopClient.DeleteSavedCredentials, IRemoteDesktopClient::DeleteSavedCredentials, rdpappcontainerclient/IRemoteDesktopClient::DeleteSavedCredentials, termserv.iremotedesktopclient_deletesavedcredentials
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
 - IRemoteDesktopClient::DeleteSavedCredentials
 - rdpappcontainerclient/IRemoteDesktopClient::DeleteSavedCredentials
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
 - IRemoteDesktopClient.DeleteSavedCredentials
---

# IRemoteDesktopClient::DeleteSavedCredentials


## -description

Deletes saved credentials for the specified remote computer.

## -parameters

### -param serverName [in]

The name of the remote computer. This can be a DNS name or an IP address.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient">IRemoteDesktopClient</a>