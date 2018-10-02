---
UID: NF:rdpappcontainerclient.IRemoteDesktopClient.DeleteSavedCredentials
title: IRemoteDesktopClient::DeleteSavedCredentials
author: windows-sdk-content
description: Deletes saved credentials for the specified remote computer.
old-location: termserv\iremotedesktopclient_deletesavedcredentials.htm
tech.root: TermServ
ms.assetid: 9addc8de-1e82-47a3-a10e-566bacc3e37c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DeleteSavedCredentials, DeleteSavedCredentials method [Remote Desktop Services], DeleteSavedCredentials method [Remote Desktop Services],IRemoteDesktopClient interface, IRemoteDesktopClient interface [Remote Desktop Services],DeleteSavedCredentials method, IRemoteDesktopClient.DeleteSavedCredentials, IRemoteDesktopClient::DeleteSavedCredentials, rdpappcontainerclient/IRemoteDesktopClient::DeleteSavedCredentials, termserv.iremotedesktopclient_deletesavedcredentials
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsTscAx.dll
api_name:
 - IRemoteDesktopClient.DeleteSavedCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRemoteDesktopClient::DeleteSavedCredentials


## -description



Deletes saved credentials for the specified remote computer.




## -parameters




### -param serverName [in]

The name of the remote computer. This can be a DNS name or an IP address.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4b4c1080-3ea1-4557-92d6-45a80a788071">IRemoteDesktopClient</a>
 

 

