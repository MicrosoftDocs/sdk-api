---
UID: NN:fsrmquota.IFsrmQuotaManager
title: IFsrmQuotaManager
author: windows-sdk-content
description: Used to manage quotas.
old-location: fsrm\ifsrmquotamanager.htm
tech.root: fsrm
ms.assetid: 20bda7d6-5c7b-4066-82e2-83ad52515568
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmQuotaManager, IFsrmQuotaManager interface [File Server Resource Manager], IFsrmQuotaManager interface [File Server Resource Manager],described, fs.ifsrmquotamanager, fsrm.ifsrmquotamanager, fsrmquota/IFsrmQuotaManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: fsrmquota.h
req.include-header: FsrmQuota.h, FsrmTlb.h
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
 - IFsrmQuotaManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaManager interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Used to manage quotas.

To get this interface, call the 
    <a href="https://msdn.microsoft.com/en-us/library/ms680701(v=VS.85).aspx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmQuotaManager</b> as the class identifier and 
    <code>__uuidof(IFsrmQuotaManager)</code> as the interface identifier. For 
    an example, see <a href="https://msdn.microsoft.com/b4471a75-f8c9-48aa-8ce3-1e998dbe6952">Defining a Quota</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuotaManager</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFsrmQuotaManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmQuotaManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/faaa55ca-a0b1-4cd4-9c73-20d80879b10c">CreateAutoApplyQuota</a>
</td>
<td align="left" width="63%">
Creates an automatic quota for the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09f0b952-e24f-4388-8e82-6b34145f9ad4">CreateQuota</a>
</td>
<td align="left" width="63%">
Creates a quota for the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88656cb9-1e72-4f82-ac09-fbb3c8a36afc">CreateQuotaCollection</a>
</td>
<td align="left" width="63%">
Creates an empty collection to which you can add quotas.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6542bc4e-535f-4e6c-aaa8-ba6963490811">EnumAutoApplyQuotas</a>
</td>
<td align="left" width="63%">
Enumerates the automatic quotas that are associated with the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abe5e73b-459a-4e2a-9917-91d3c85a15bc">EnumEffectiveQuotas</a>
</td>
<td align="left" width="63%">
Enumerates all the quotas that affect the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9977a519-4a6d-4b35-b973-4ef086e13e92">EnumQuotas</a>
</td>
<td align="left" width="63%">
Enumerates the quotas that are associated with the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6a4645c-c323-4c28-a284-9ebb677aeebb">GetAutoApplyQuota</a>
</td>
<td align="left" width="63%">
Retrieves the automatic quota for the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c595714-20c9-4ca5-96a2-64b7a7c6f84e">GetQuota</a>
</td>
<td align="left" width="63%">
Retrieves the quota for the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa1ac69d-341e-49fd-893c-82ce3577c1f5">GetRestrictiveQuota</a>
</td>
<td align="left" width="63%">
Retrieves the most restrictive quota for the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1581f4c7-a912-4214-9ad9-181ad5ebba7e">Scan</a>
</td>
<td align="left" width="63%">
Starts a quota scan on the specified path.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuotaManager</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/39e2efcb-fbed-48aa-a1ea-481df6fe2ea6">ActionVariableDescriptions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the descriptions for the macros contained in the 
     <a href="https://msdn.microsoft.com/e7fe0139-692b-4f88-8411-ffd31d29e40d">ActionVariables</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e7fe0139-692b-4f88-8411-ffd31d29e40d">ActionVariables</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a  list of macros that you can specify in action property values.

</td>
</tr>
</table> 


## -remarks



A directory quota restricts the size of a specific directory to a configurable quota limit. In addition to 
    the limit, a directory quota may be configured with one or more directory quota thresholds which define a set of 
    actions that are initiated when the quota usage reaches the threshold value.

You can create a quota, an automatic quota, or a quota template. A quota applies to a specific directory. The 
    automatic quota applies to the specified directory and automatically creates quotas for new and existing 
    subdirectories of the specified directory. The quota template is used to modify properties in bulk by applying 
    the changes to quotas that derive from the quota template.

Note that if the directory is renamed, the quota applies to the renamed directory. If the directory is 
    deleted, the quota is deleted.

To create this object from a script, use the program identifier, 
    "Fsrm.FsrmQuotaManager".




## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/a61a4797-b3f5-4f50-9b7c-6e30d4615b56">FsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/aa665a9d-d053-49e4-82a7-d6ba27406a7c">IFsrmQuotaManagerEx</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

