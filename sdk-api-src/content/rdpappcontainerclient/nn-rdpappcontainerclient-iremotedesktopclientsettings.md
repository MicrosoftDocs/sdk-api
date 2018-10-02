---
UID: NN:rdpappcontainerclient.IRemoteDesktopClientSettings
title: IRemoteDesktopClientSettings
author: windows-sdk-content
description: Provides the methods needed to configure the connection settings for the Remote Desktop Protocol (RDP) app container client control.
old-location: termserv\iremotedesktopclientsettings.htm
tech.root: TermServ
ms.assetid: 8bdb224c-bb29-43f1-8a7c-94686a8efe0a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IRemoteDesktopClientSettings, IRemoteDesktopClientSettings interface [Remote Desktop Services], IRemoteDesktopClientSettings interface [Remote Desktop Services],described, rdpappcontainerclient/IRemoteDesktopClientSettings, termserv.iremotedesktopclientsettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRemoteDesktopClientSettings interface


## -description


Provides the methods needed to configure the connection settings for the Remote Desktop Protocol (RDP) app container client control.

Use the <a href="https://msdn.microsoft.com/4b4c1080-3ea1-4557-92d6-45a80a788071">IRemoteDesktopClient</a>
<a href="https://msdn.microsoft.com/59999489-9ad0-4b85-9643-3b8355b817c2">Settings</a> property to obtain a pointer to this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRemoteDesktopClientSettings</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IRemoteDesktopClientSettings</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/24f17f50-6cb0-422a-88c6-77bae48af392">ApplySettings</a>
</td>
<td align="left" width="63%">
Stores the specified contents in the RDP file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e172098a-d3c1-46cc-8c46-cdf14c46b43a">GetRdpProperty</a>
</td>
<td align="left" width="63%">
Retrieves a single named RDP property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c28a172-42f3-4abd-9983-ee5acb1c9c78">RetrieveSettings</a>
</td>
<td align="left" width="63%">
Retrieves the entire RDP file as a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c1a9e70-3e77-4f21-b3a1-8e4c3c5cf148">SetRdpProperty</a>
</td>
<td align="left" width="63%">
Sets the value of a single named RDP property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/EAF75483-90A4-4BB1-82A5-EFBB2219A55B">Remote Desktop ActiveX control reference</a>
 

 

