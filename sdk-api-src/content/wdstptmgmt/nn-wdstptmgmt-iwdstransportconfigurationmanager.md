---
UID: NN:wdstptmgmt.IWdsTransportConfigurationManager
title: IWdsTransportConfigurationManager (wdstptmgmt.h)
description: Manages the configuration of a WDS transport server.helpviewer_keywords: ["IWdsTransportConfigurationManager","IWdsTransportConfigurationManager interface [Windows Deployment Services]","IWdsTransportConfigurationManager interface [Windows Deployment Services]","described","wds.iwdstransportconfigurationmanager","wdstptmgmt/IWdsTransportConfigurationManager"]
old-location: wds\iwdstransportconfigurationmanager.htm
tech.root: wds
ms.assetid: b86f9bc7-ddee-4d18-b5cb-28d28fa7ae7e
ms.date: 12/05/2018
ms.keywords: IWdsTransportConfigurationManager, IWdsTransportConfigurationManager interface [Windows Deployment Services], IWdsTransportConfigurationManager interface [Windows Deployment Services],described, wds.iwdstransportconfigurationmanager, wdstptmgmt/IWdsTransportConfigurationManager
f1_keywords:
- wdstptmgmt/IWdsTransportConfigurationManager
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWdsTransportConfigurationManager interface


## -description


Manages the configuration of a WDS transport server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportConfigurationManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWdsTransportConfigurationManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportconfigurationmanager-disablewdstransportservices">DisableWdsTransportServices</a>
</td>
<td align="left" width="63%">
Sets all WDS transport services to Disabled mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportconfigurationmanager-enablewdstransportservices">EnableWdsTransportServices</a>
</td>
<td align="left" width="63%">
Sets all WDS transport services to Auto-Start mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportconfigurationmanager-notifywdstransportservices">NotifyWdsTransportServices</a>
</td>
<td align="left" width="63%">
Sends a notification to WDS transport services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportconfigurationmanager-restartwdstransportservices">RestartWdsTransportServices</a>
</td>
<td align="left" width="63%">
Stops and then restarts any WDS transport services that are running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportconfigurationmanager-startwdstransportservices">StartWdsTransportServices</a>
</td>
<td align="left" width="63%">
Starts all WDS transport services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportconfigurationmanager-stopwdstransportservices">StopWdsTransportServices</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportconfigurationmanager-get_diagnosticspolicy">DiagnosticsPolicy</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportconfigurationmanager-get_servicepolicy">ServicePolicy</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportconfigurationmanager-get_wdstransportservicesrunning">WdsTransportServicesRunning</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a value that indicates whether WDS transport services are running on the server.

</td>
</tr>
</table> 

