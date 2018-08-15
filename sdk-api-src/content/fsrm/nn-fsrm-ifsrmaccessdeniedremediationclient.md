---
UID: NN:fsrm.IFsrmAccessDeniedRemediationClient
title: IFsrmAccessDeniedRemediationClient
author: windows-sdk-content
description: Used to show the Access Denied Remediation (ADR) client user interface.
old-location: fsrm\ifsrmaccessdeniedremediationclient.htm
old-project: fsrm
ms.assetid: 572d2985-a579-4bfa-a305-403b6be516ca
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmAccessDeniedRemediationClient, IFsrmAccessDeniedRemediationClient interface [File Server Resource Manager], IFsrmAccessDeniedRemediationClient interface [File Server Resource Manager],described, fs.ifsrmaccessdeniedremediationclient, fsrm.ifsrmaccessdeniedremediationclient, fsrm/IFsrmAccessDeniedRemediationClient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmAccessDeniedRemediationClient
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmAccessDeniedRemediationClient</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFsrmAccessDeniedRemediationClient</b> also has these types of members:
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
 

 

