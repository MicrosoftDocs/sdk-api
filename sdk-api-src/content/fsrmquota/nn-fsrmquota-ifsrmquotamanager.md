---
UID: NN:fsrmquota.IFsrmQuotaManager
title: IFsrmQuotaManager (fsrmquota.h)
author: windows-sdk-content
description: Used to manage quotas.
old-location: fsrm\ifsrmquotamanager.htm
tech.root: fsrm
ms.assetid: 20bda7d6-5c7b-4066-82e2-83ad52515568
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaManager, IFsrmQuotaManager interface [File Server Resource Manager], IFsrmQuotaManager interface [File Server Resource Manager],described, fs.ifsrmquotamanager, fsrm.ifsrmquotamanager, fsrmquota/IFsrmQuotaManager
ms.topic: interface
f1_keywords: 
 - "fsrmquota/IFsrmQuotaManager"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmQuotaManager interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Used to manage quotas.

To get this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmQuotaManager</b> as the class identifier and 
    <code>__uuidof(IFsrmQuotaManager)</code> as the interface identifier. For 
    an example, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/defining-a-quota">Defining a Quota</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuotaManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmQuotaManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-createautoapplyquota">CreateAutoApplyQuota</a>
</td>
<td align="left" width="63%">
Creates an automatic quota for the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-createquota">CreateQuota</a>
</td>
<td align="left" width="63%">
Creates a quota for the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-createquotacollection">CreateQuotaCollection</a>
</td>
<td align="left" width="63%">
Creates an empty collection to which you can add quotas.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumautoapplyquotas">EnumAutoApplyQuotas</a>
</td>
<td align="left" width="63%">
Enumerates the automatic quotas that are associated with the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumeffectivequotas">EnumEffectiveQuotas</a>
</td>
<td align="left" width="63%">
Enumerates all the quotas that affect the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumquotas">EnumQuotas</a>
</td>
<td align="left" width="63%">
Enumerates the quotas that are associated with the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-getautoapplyquota">GetAutoApplyQuota</a>
</td>
<td align="left" width="63%">
Retrieves the automatic quota for the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-getquota">GetQuota</a>
</td>
<td align="left" width="63%">
Retrieves the quota for the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-getrestrictivequota">GetRestrictiveQuota</a>
</td>
<td align="left" width="63%">
Retrieves the most restrictive quota for the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-scan">Scan</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-get_actionvariabledescriptions">ActionVariableDescriptions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the descriptions for the macros contained in the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-get_actionvariables">ActionVariables</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-get_actionvariables">ActionVariables</a>


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
 

 

