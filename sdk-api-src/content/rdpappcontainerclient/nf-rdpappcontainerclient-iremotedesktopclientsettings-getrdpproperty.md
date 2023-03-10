---
UID: NF:rdpappcontainerclient.IRemoteDesktopClientSettings.GetRdpProperty
title: IRemoteDesktopClientSettings::GetRdpProperty (rdpappcontainerclient.h)
description: Retrieves a single named RDP property value.
helpviewer_keywords: ["GetRdpProperty","GetRdpProperty method [Remote Desktop Services]","GetRdpProperty method [Remote Desktop Services]","IRemoteDesktopClientSettings interface","IRemoteDesktopClientSettings interface [Remote Desktop Services]","GetRdpProperty method","IRemoteDesktopClientSettings.GetRdpProperty","IRemoteDesktopClientSettings::GetRdpProperty","rdpappcontainerclient/IRemoteDesktopClientSettings::GetRdpProperty","termserv.iremotedesktopclientsettings_getrdpproperty"]
old-location: termserv\iremotedesktopclientsettings_getrdpproperty.htm
tech.root: TermServ
ms.assetid: e172098a-d3c1-46cc-8c46-cdf14c46b43a
ms.date: 12/05/2018
ms.keywords: GetRdpProperty, GetRdpProperty method [Remote Desktop Services], GetRdpProperty method [Remote Desktop Services],IRemoteDesktopClientSettings interface, IRemoteDesktopClientSettings interface [Remote Desktop Services],GetRdpProperty method, IRemoteDesktopClientSettings.GetRdpProperty, IRemoteDesktopClientSettings::GetRdpProperty, rdpappcontainerclient/IRemoteDesktopClientSettings::GetRdpProperty, termserv.iremotedesktopclientsettings_getrdpproperty
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
 - IRemoteDesktopClientSettings::GetRdpProperty
 - rdpappcontainerclient/IRemoteDesktopClientSettings::GetRdpProperty
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
 - IRemoteDesktopClientSettings.GetRdpProperty
---

# IRemoteDesktopClientSettings::GetRdpProperty


## -description

Retrieves a single named RDP property value. If the specified property has not been set, a default value is retrieved.

## -parameters

### -param propertyName [in]

### -param value [out, retval]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclientsettings">IRemoteDesktopClientSettings</a>