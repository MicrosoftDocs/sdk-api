---
UID: NN:wdstptmgmt.IWdsTransportConfigurationManager
title: IWdsTransportConfigurationManager (wdstptmgmt.h)
author: windows-sdk-content
description: Manages the configuration of a WDS transport server.
old-location: wds\iwdstransportconfigurationmanager.htm
tech.root: wds
ms.assetid: b86f9bc7-ddee-4d18-b5cb-28d28fa7ae7e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWdsTransportConfigurationManager, IWdsTransportConfigurationManager interface [Windows Deployment Services], IWdsTransportConfigurationManager interface [Windows Deployment Services],described, wds.iwdstransportconfigurationmanager, wdstptmgmt/IWdsTransportConfigurationManager
ms.topic: interface
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportConfigurationManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWdsTransportConfigurationManager interface


## -description


Manages the configuration of a WDS transport server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportConfigurationManager</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWdsTransportConfigurationManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWdsTransportConfigurationManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46ded55b-f371-405a-bfcd-c361ac6fb5bd">DisableWdsTransportServices</a>
</td>
<td align="left" width="63%">
Sets all WDS transport services to Disabled mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30f4ff61-8e92-4d1b-8243-e5cc9d64da40">EnableWdsTransportServices</a>
</td>
<td align="left" width="63%">
Sets all WDS transport services to Auto-Start mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ca38fe9-fc18-41f1-bd4b-5e3e84e496d0">NotifyWdsTransportServices</a>
</td>
<td align="left" width="63%">
Sends a notification to WDS transport services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0aa84fa-f2a6-4494-8994-89854565fd7b">RestartWdsTransportServices</a>
</td>
<td align="left" width="63%">
Stops and then restarts any WDS transport services that are running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7612335a-4d81-4ec5-a348-93adefb0cced">StartWdsTransportServices</a>
</td>
<td align="left" width="63%">
Starts all WDS transport services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/510dff2a-a459-4694-9c68-802d703ff716">StopWdsTransportServices</a>
</td>
<td align="left" width="63%">
Stops all WDS transport services.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportConfigurationManager</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/80a84495-724c-4198-8262-dcf8cabce3f0">DiagnosticsPolicy</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives an interface pointer to the Configuration Manager's Diagnostics Policy object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3ee3abe8-3ac4-409c-b994-023b0c4c6f72">ServicePolicy</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives an interface pointer to the Configuration Manager's Service Policy object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0296a818-1a5f-494c-869a-a124fc75cb85">WdsTransportServicesRunning</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a value that indicates whether WDS transport services are running on the server.

</td>
</tr>
</table> 

