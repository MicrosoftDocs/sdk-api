---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFsrmAccessDeniedRemediationClient interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/fec0343f-4ab6-4b8c-b365-e510286af2be">MSFT_FSRMAdr</a> and 
    <a href="https://msdn.microsoft.com/0ddadb89-7059-43bb-9b8b-e31976ce715a">MSFT_FSRMADRSettings</a> classes.]

Used to show the Access Denied Remediation (ADR) client user interface.

This interface was introduced for applications that are already using the FSRM interfaces. Where possible it is 
    recommended to use the <a href="https://msdn.microsoft.com/fec0343f-4ab6-4b8c-b365-e510286af2be">MSFT_FSRMAdr</a> and 
    <a href="https://msdn.microsoft.com/0ddadb89-7059-43bb-9b8b-e31976ce715a">MSFT_FSRMADRSettings</a> WMI classes instead.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmAccessDeniedRemediationClient</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmAccessDeniedRemediationClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmAccessDeniedRemediationClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/befebb2a-99a1-4a32-8bde-3b263d1f4459">Show</a>
</td>
<td align="left" width="63%">
Displays the Access Denied Remediation client user interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/0ddadb89-7059-43bb-9b8b-e31976ce715a">MSFT_FSRMADRSettings</a>



<a href="https://msdn.microsoft.com/fec0343f-4ab6-4b8c-b365-e510286af2be">MSFT_FSRMAdr</a>
 

 

