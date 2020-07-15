---
UID: NN:rdpappcontainerclient.IRemoteDesktopClientSettings
title: IRemoteDesktopClientSettings (rdpappcontainerclient.h)
description: Provides the methods needed to configure the connection settings for the Remote Desktop Protocol (RDP) app container client control.
helpviewer_keywords: ["IRemoteDesktopClientSettings","IRemoteDesktopClientSettings interface [Remote Desktop Services]","IRemoteDesktopClientSettings interface [Remote Desktop Services]","described","rdpappcontainerclient/IRemoteDesktopClientSettings","termserv.iremotedesktopclientsettings"]
old-location: termserv\iremotedesktopclientsettings.htm
tech.root: TermServ
ms.assetid: 8bdb224c-bb29-43f1-8a7c-94686a8efe0a
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClientSettings, IRemoteDesktopClientSettings interface [Remote Desktop Services], IRemoteDesktopClientSettings interface [Remote Desktop Services],described, rdpappcontainerclient/IRemoteDesktopClientSettings, termserv.iremotedesktopclientsettings
f1_keywords:
- rdpappcontainerclient/IRemoteDesktopClientSettings
dev_langs:
- c++
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
- IRemoteDesktopClientSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRemoteDesktopClientSettings interface


## -description


Provides the methods needed to configure the connection settings for the Remote Desktop Protocol (RDP) app container client control.

Use the <a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient">IRemoteDesktopClient</a>
<a href="https://docs.microsoft.com/windows/desktop/TermServ/iremotedesktopclient-settings">Settings</a> property to obtain a pointer to this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRemoteDesktopClientSettings</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRemoteDesktopClientSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRemoteDesktopClientSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientsettings-applysettings">ApplySettings</a>
</td>
<td align="left" width="63%">
Stores the specified contents in the RDP file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientsettings-getrdpproperty">GetRdpProperty</a>
</td>
<td align="left" width="63%">
Retrieves a single named RDP property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientsettings-retrievesettings">RetrieveSettings</a>
</td>
<td align="left" width="63%">
Retrieves the entire RDP file as a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclientsettings-setrdpproperty">SetRdpProperty</a>
</td>
<td align="left" width="63%">
Sets the value of a single named RDP property.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-activex-control-reference">Remote Desktop ActiveX control reference</a>
 

 

