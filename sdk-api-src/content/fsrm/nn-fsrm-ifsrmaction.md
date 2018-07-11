---
UID: NN:fsrm.IFsrmAction
title: IFsrmAction
author: windows-sdk-content
description: The base class for all FSRM action interfaces.
old-location: fsrm\ifsrmaction.htm
old-project: fsrm
ms.assetid: 81bfae1d-7d09-4ddc-9669-1da40dc72fd4
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IFsrmAction, IFsrmAction interface [File Server Resource Manager], IFsrmAction interface [File Server Resource Manager],described, fs.ifsrmaction, fsrm.ifsrmaction, fsrm/IFsrmAction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IFsrmAction
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmAction interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

The base class for all FSRM action interfaces.

To create an action, call one of the following methods:
<ul>
<li>
<a href="https://msdn.microsoft.com/d0cb2ac1-842c-4ebb-adac-8298a0e0beed">IFsrmFileManagementJob::CreateNotificationAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d627e07-fa8c-4c22-acba-c08767b8ebaa">IFsrmFileScreenBase::CreateAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/27813041-ee42-4412-982e-fce594c5e648">IFsrmQuotaBase::CreateThresholdAction</a>
</li>
</ul>Then, call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method of the 
    returned interface for an interface of the specific action type. For an example, see 
    <a href="https://msdn.microsoft.com/45b16b46-7c03-4af5-889f-64047ec5ca98">Performing Actions Based on File Screen Violations</a>.

The following methods return a collection of actions:
<ul>
<li>
<a href="https://msdn.microsoft.com/cfb58db2-39af-434e-95e2-abbd21f4487a">IFsrmFileManagementJob::EnumNotificationActions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fbc22338-8271-407a-97c6-4a2329445979">IFsrmFileScreenBase::EnumActions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ce4f85a9-f2e0-42df-adb4-7c21256d5305">IFsrmQuotaBase::EnumThresholdActions</a>
</li>
</ul>To get this interface from an item of the collection, call the 
    <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on the 
    <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface contained in the 
    <b>pdispVal</b> member of the variant.

Use the <a href="https://msdn.microsoft.com/7ce0bafb-8076-4a0d-bd59-9e2d436f74c1">ActionType</a> property to determine the 
    type of action that this interface defines. You can then call the 
    <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on this interface to get an 
    interface that defines the action type. The See Also section lists the possible interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmAction</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmAction</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/66d17a40-704d-46e6-b8bb-ae7f80e52fa5">Delete</a>
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

<a href="https://msdn.microsoft.com/7ce0bafb-8076-4a0d-bd59-9e2d436f74c1">ActionType</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a>


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

<a href="https://msdn.microsoft.com/3d5be77f-282f-479d-aa34-a8cb1c771951">RunLimitInterval</a>


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




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/b7f9fc8c-2f55-4a0e-879a-64c368abcabb">IFsrmActionCommand</a>



<a href="https://msdn.microsoft.com/6eb6d82e-018d-4977-ad60-fce296c16e83">IFsrmActionEmail</a>



<a href="https://msdn.microsoft.com/278ef98d-fb1d-42a4-a740-07c5e713a230">IFsrmActionEmail2</a>



<a href="https://msdn.microsoft.com/418cd7aa-c363-4ab7-9c7e-2d0388483a8f">IFsrmActionEventLog</a>



<a href="https://msdn.microsoft.com/efff4cec-6985-40aa-a74e-bb2afdeb2a0a">IFsrmActionReport</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

