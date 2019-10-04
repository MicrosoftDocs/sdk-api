---
UID: NN:fsrm.IFsrmAction
title: IFsrmAction (fsrm.h)
author: windows-sdk-content
description: The base class for all FSRM action interfaces.
old-location: fsrm\ifsrmaction.htm
tech.root: fsrm
ms.assetid: 81bfae1d-7d09-4ddc-9669-1da40dc72fd4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmAction, IFsrmAction interface [File Server Resource Manager], IFsrmAction interface [File Server Resource Manager],described, fs.ifsrmaction, fsrm.ifsrmaction, fsrm/IFsrmAction
ms.topic: interface
f1_keywords: 
 - "fsrm/IFsrmAction"
dev_langs:
 - c++
req.header: fsrm.h
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
 - IFsrmAction
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmAction interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

The base class for all FSRM action interfaces.

To create an action, call one of the following methods:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createnotificationaction">IFsrmFileManagementJob::CreateNotificationAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-createaction">IFsrmFileScreenBase::CreateAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-createthresholdaction">IFsrmQuotaBase::CreateThresholdAction</a>
</li>
</ul>Then, call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method of the 
    returned interface for an interface of the specific action type. For an example, see 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/performing-actions-based-on-file-screen-violations">Performing Actions Based on File Screen Violations</a>.

The following methods return a collection of actions:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-enumnotificationactions">IFsrmFileManagementJob::EnumNotificationActions</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-enumactions">IFsrmFileScreenBase::EnumActions</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-enumthresholdactions">IFsrmQuotaBase::EnumThresholdActions</a>
</li>
</ul>To get this interface from an item of the collection, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method on the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface contained in the 
    <b>pdispVal</b> member of the variant.

Use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-get_actiontype">ActionType</a> property to determine the 
    type of action that this interface defines. You can then call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method on this interface to get an 
    interface that defines the action type. The See Also section lists the possible interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmAction</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmAction</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmAction</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-delete">Delete</a>
</td>
<td align="left" width="63%">
Removes the action from the quota or file screen object's list of actions.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmAction</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-get_actiontype">ActionType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the action's type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-get_id">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the identifier of the action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-get_runlimitinterval">RunLimitInterval</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the interval that must expire before the action is run again.

</td>
</tr>
</table> 


## -remarks



The FSRM server starts the action in response to quota or file screen event (for example, a directory size 
    exceeds a directory quota threshold or detection of a restricted file).




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail">IFsrmActionEmail</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail2">IFsrmActionEmail2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioneventlog">IFsrmActionEventLog</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionreport">IFsrmActionReport</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
 

 

