---
UID: NF:rdpappcontainerclient.IRemoteDesktopClientSettings.RetrieveSettings
title: IRemoteDesktopClientSettings::RetrieveSettings (rdpappcontainerclient.h)
author: windows-sdk-content
description: Retrieves the entire RDP file as a string.
old-location: termserv\iremotedesktopclientsettings_retrievesettings.htm
tech.root: TermServ
ms.assetid: 5c28a172-42f3-4abd-9983-ee5acb1c9c78
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClientSettings interface [Remote Desktop Services],RetrieveSettings method, IRemoteDesktopClientSettings.RetrieveSettings, IRemoteDesktopClientSettings::RetrieveSettings, RetrieveSettings, RetrieveSettings method [Remote Desktop Services], RetrieveSettings method [Remote Desktop Services],IRemoteDesktopClientSettings interface, rdpappcontainerclient/IRemoteDesktopClientSettings::RetrieveSettings, termserv.iremotedesktopclientsettings_retrievesettings
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
 - IRemoteDesktopClientSettings.RetrieveSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRemoteDesktopClientSettings::RetrieveSettings


## -description



Retrieves the entire RDP file as a string.




## -parameters




### -param rdpFileContents [out, retval]

The entire contents of the RDP file.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8bdb224c-bb29-43f1-8a7c-94686a8efe0a">IRemoteDesktopClientSettings</a>
 

 

