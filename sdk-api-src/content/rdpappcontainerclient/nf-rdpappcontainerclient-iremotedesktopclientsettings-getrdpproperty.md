---
UID: NF:rdpappcontainerclient.IRemoteDesktopClientSettings.GetRdpProperty
title: IRemoteDesktopClientSettings::GetRdpProperty
author: windows-sdk-content
description: Retrieves a single named RDP property value.
old-location: termserv\iremotedesktopclientsettings_getrdpproperty.htm
tech.root: termserv
ms.assetid: e172098a-d3c1-46cc-8c46-cdf14c46b43a
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetRdpProperty, GetRdpProperty method [Remote Desktop Services], GetRdpProperty method [Remote Desktop Services],IRemoteDesktopClientSettings interface, IRemoteDesktopClientSettings interface [Remote Desktop Services],GetRdpProperty method, IRemoteDesktopClientSettings.GetRdpProperty, IRemoteDesktopClientSettings::GetRdpProperty, rdpappcontainerclient/IRemoteDesktopClientSettings::GetRdpProperty, termserv.iremotedesktopclientsettings_getrdpproperty
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
 - IRemoteDesktopClientSettings.GetRdpProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRemoteDesktopClientSettings::GetRdpProperty


## -description


Retrieves a single named RDP property value. If the specified property has not been set, a default value is retrieved.


## -parameters




### -param propertyName [in]


### -param value

TBD




#### - Value [out, retval]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8bdb224c-bb29-43f1-8a7c-94686a8efe0a">IRemoteDesktopClientSettings</a>
 

 

