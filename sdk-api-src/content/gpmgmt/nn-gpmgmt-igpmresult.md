---
UID: NN:gpmgmt.IGPMResult
title: IGPMResult (gpmgmt.h)
description: The IGPMResult interface contains methods to retrieve status message information while performing various types of GPO processing operations such as restore, import, copy and backup.
old-location: gpmc\igpmresult.htm
tech.root: gpmc
ms.assetid: 0228ed1a-3a8f-486a-9dd8-806ca35c649e
ms.date: 12/05/2018
ms.keywords: GPMResult, IGPMResult, IGPMResult interface [GPMC], IGPMResult interface [GPMC],described, _win32_igpmresult, gpmc.igpmresult, gpmgmt/IGPMResult
ms.topic: interface
f1_keywords:
- gpmgmt/IGPMResult
dev_langs:
- c++
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gpmgmt.dll
api_name:
- IGPMResult
- GPMResult
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMResult interface


## -description


The 
<b>IGPMResult</b> interface contains methods to retrieve status message information while performing various types of GPO processing operations such as restore, import, copy and backup.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMResult</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmresult-overallstatus">OverallStatus</a>
</td>
<td align="left" width="63%">
Returns the overall status of the GPMC operation.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMResult</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmresult-property-methods">Result</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Pointer to a <b>VARIANT</b> that receives the result of various types of GPO operations. This property is the location at which an <b>IDispatch</b> interface pointer can be stored.

For calls to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-backup">IGPMGPO::Backup</a> method, the result is a pointer to an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> interface. For calls to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-restoregpo">IGPMDomain::RestoreGPO</a>, 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-import">IGPMGPO::Import</a>, and 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-copyto">IGPMGPO::CopyTo</a>, the result is a pointer to an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a> interface. For calls to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-generatereport">IGPMGPO::GenerateReport</a> method, the result contains a binary string of XML or HTML.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmresult-property-methods">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Pointer to an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>
 

 

