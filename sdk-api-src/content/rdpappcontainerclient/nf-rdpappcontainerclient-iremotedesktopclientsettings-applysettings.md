---
UID: NF:rdpappcontainerclient.IRemoteDesktopClientSettings.ApplySettings
title: IRemoteDesktopClientSettings::ApplySettings (rdpappcontainerclient.h)
description: Stores the specified contents in the RDP file.
helpviewer_keywords: ["ApplySettings","ApplySettings method [Remote Desktop Services]","ApplySettings method [Remote Desktop Services]","IRemoteDesktopClientSettings interface","IRemoteDesktopClientSettings interface [Remote Desktop Services]","ApplySettings method","IRemoteDesktopClientSettings.ApplySettings","IRemoteDesktopClientSettings::ApplySettings","rdpappcontainerclient/IRemoteDesktopClientSettings::ApplySettings","termserv.iremotedesktopclientsettings_applysettings"]
old-location: termserv\iremotedesktopclientsettings_applysettings.htm
tech.root: TermServ
ms.assetid: 24f17f50-6cb0-422a-88c6-77bae48af392
ms.date: 12/05/2018
ms.keywords: ApplySettings, ApplySettings method [Remote Desktop Services], ApplySettings method [Remote Desktop Services],IRemoteDesktopClientSettings interface, IRemoteDesktopClientSettings interface [Remote Desktop Services],ApplySettings method, IRemoteDesktopClientSettings.ApplySettings, IRemoteDesktopClientSettings::ApplySettings, rdpappcontainerclient/IRemoteDesktopClientSettings::ApplySettings, termserv.iremotedesktopclientsettings_applysettings
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
 - IRemoteDesktopClientSettings::ApplySettings
 - rdpappcontainerclient/IRemoteDesktopClientSettings::ApplySettings
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
 - IRemoteDesktopClientSettings.ApplySettings
---

# IRemoteDesktopClientSettings::ApplySettings


## -description

Stores the specified contents in the RDP file.

## -parameters

### -param rdpFileContents [in]

Specifies the entire contents of the RDP file.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclientsettings">IRemoteDesktopClientSettings</a>