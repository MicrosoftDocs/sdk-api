---
UID: NN:fsrmquota.IFsrmQuotaBase
title: IFsrmQuotaBase
author: windows-sdk-content
description: Base interface for all quota interfaces.
old-location: fsrm\ifsrmquotabase.htm
tech.root: fsrm
ms.assetid: 7f4d5a73-a836-4ea1-bc53-d51433eeb02e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmQuotaBase, IFsrmQuotaBase interface [File Server Resource Manager], IFsrmQuotaBase interface [File Server Resource Manager],described, fs.ifsrmquotabase, fsrm.ifsrmquotabase, fsrm/IFsrmQuotaBase
ms.topic: interface
req.header: fsrmquota.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmQuotaBase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaBase interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Base interface for all quota interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuotaBase</b> interface inherits from <a href="https://msdn.microsoft.com/bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7">IFsrmObject</a>. <b>IFsrmQuotaBase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmQuotaBase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9571e169-01a3-4b72-bc84-2f9b2609a6e2">AddThreshold</a>
</td>
<td align="left" width="63%">
Adds a threshold to the quota object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27813041-ee42-4412-982e-fce594c5e648">CreateThresholdAction</a>
</td>
<td align="left" width="63%">
Creates an action and associates it with the specified threshold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f6ace15-05aa-4276-88eb-3a4315b3b51c">DeleteThreshold</a>
</td>
<td align="left" width="63%">
Deletes a threshold from the quota object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce4f85a9-f2e0-42df-adb4-7c21256d5305">EnumThresholdActions</a>
</td>
<td align="left" width="63%">
Enumerates all the actions for the specified threshold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46cda78a-7c1d-42e0-abff-3be9c13925f5">ModifyThreshold</a>
</td>
<td align="left" width="63%">
Changes  the threshold value.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuotaBase</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/af856281-8161-4165-bf24-0c160f7394d2">QuotaFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the quota flags for the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2f2b5d8f-70b7-497e-9c51-171dca657c69">QuotaLimit</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the quota limit for the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e9a68b62-5d53-419f-a0c4-2e284fa51313">Thresholds</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the thresholds for the quota object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7">IFsrmObject</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

