---
UID: NN:fsrm.IFsrmCollection
title: IFsrmCollection
author: windows-sdk-content
description: Defines a collection of FSRM objects.
old-location: fsrm\ifsrmcollection.htm
old-project: Fsrm
ms.assetid: 6a0c5d8b-5fed-4c55-971c-43430e3c6a8d
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmCollection, IFsrmCollection interface [File Server Resource Manager], IFsrmCollection interface [File Server Resource Manager],described, fs.ifsrmcollection, fsrm.ifsrmcollection, fsrm/IFsrmCollection
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmCollection interface


## -description


Defines a collection of FSRM objects.

The following methods and properties return this collection:
<ul>
<li>
<a href="https://msdn.microsoft.com/844cb2a5-8526-434b-af22-b1bf856ed6af">IFsrmCommittableCollection::Commit</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9859a7e1-ebfe-4b6c-bd89-93757e1b4684">IFsrmDerivedObjectsResult::DerivedObjects</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b5946160-565b-4c94-ba2e-18f270eb1af1">IFsrmDerivedObjectsResult::Results</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fbc22338-8271-407a-97c6-4a2329445979">IFsrmFileScreenBase::EnumActions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d9d726ea-62f7-489e-a442-c8719648e893">IFsrmPropertyDefinition2::ValueDefinitions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ce4f85a9-f2e0-42df-adb4-7c21256d5305">IFsrmQuotaBase::EnumThresholdActions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a1292084-f1b5-43eb-9b59-fa2f3f99557d">IFsrmReportJob::EnumReports</a>
</li>
<li>
<a href="https://msdn.microsoft.com/af66beb6-e82c-47e6-8658-da9702041053">IFsrmReportManager::EnumReportJobs</a>
</li>
</ul>The collection is empty if the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a> property is 
    zero.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the collection of objects when the objects are collected asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d6be809-bfe6-46ad-9156-288da834ff13">GetById</a>
</td>
<td align="left" width="63%">
Retrieves the specified object from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83b9feb5-5f10-4c27-be3e-b267a0356aa2">WaitForCompletion</a>
</td>
<td align="left" width="63%">
Limits the time that the collection can take to collect the objects.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="_com_IUnknown">IUnknown</a> pointer of a new 
     <a href="https://msdn.microsoft.com/139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> enumeration for the items 
     in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the requested item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c12c55c1-baff-4810-ad2a-453abb6af5b5">State</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the state of the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/844cb2a5-8526-434b-af22-b1bf856ed6af">IFsrmCommittableCollection::Commit</a>



<a href="https://msdn.microsoft.com/9859a7e1-ebfe-4b6c-bd89-93757e1b4684">IFsrmDerivedObjectsResult::DerivedObjects</a>



<a href="https://msdn.microsoft.com/b5946160-565b-4c94-ba2e-18f270eb1af1">IFsrmDerivedObjectsResult::Results</a>



<a href="https://msdn.microsoft.com/fbc22338-8271-407a-97c6-4a2329445979">IFsrmFileScreenBase::EnumActions</a>



<a href="https://msdn.microsoft.com/d9d726ea-62f7-489e-a442-c8719648e893">IFsrmPropertyDefinition2::ValueDefinitions</a>



<a href="https://msdn.microsoft.com/ce4f85a9-f2e0-42df-adb4-7c21256d5305">IFsrmQuotaBase::EnumThresholdActions</a>



<a href="https://msdn.microsoft.com/a1292084-f1b5-43eb-9b59-fa2f3f99557d">IFsrmReportJob::EnumReports</a>



<a href="https://msdn.microsoft.com/af66beb6-e82c-47e6-8658-da9702041053">IFsrmReportManager::EnumReportJobs</a>
 

 

