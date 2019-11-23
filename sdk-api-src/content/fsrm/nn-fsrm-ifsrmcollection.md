---
UID: NN:fsrm.IFsrmCollection
title: IFsrmCollection (fsrm.h)

description: Defines a collection of FSRM objects.
old-location: fsrm\ifsrmcollection.htm
tech.root: fsrm
ms.assetid: 6a0c5d8b-5fed-4c55-971c-43430e3c6a8d

ms.date: 12/05/2018
ms.keywords: IFsrmCollection, IFsrmCollection interface [File Server Resource Manager], IFsrmCollection interface [File Server Resource Manager],described, fs.ifsrmcollection, fsrm.ifsrmcollection, fsrm/IFsrmCollection
ms.topic: interface
f1_keywords: 
 - "fsrm/IFsrmCollection"
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
 - IFsrmCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmCollection interface


## -description


Defines a collection of FSRM objects.

The following methods and properties return this collection:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcommittablecollection-commit">IFsrmCommittableCollection::Commit</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmderivedobjectsresult-get_derivedobjects">IFsrmDerivedObjectsResult::DerivedObjects</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmderivedobjectsresult-get_results">IFsrmDerivedObjectsResult::Results</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-enumactions">IFsrmFileScreenBase::EnumActions</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition2-get_valuedefinitions">IFsrmPropertyDefinition2::ValueDefinitions</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-enumthresholdactions">IFsrmQuotaBase::EnumThresholdActions</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-enumreports">IFsrmReportJob::EnumReports</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-enumreportjobs">IFsrmReportManager::EnumReportJobs</a>
</li>
</ul>The collection is empty if the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-get_count">Count</a> property is 
    zero.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmCollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the collection of objects when the objects are collected asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-getbyid">GetById</a>
</td>
<td align="left" width="63%">
Retrieves the specified object from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-waitforcompletion">WaitForCompletion</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer of a new 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> enumeration for the items 
     in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-get_count">Count</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-get_item">Item</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-get_state">State</a>


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcommittablecollection-commit">IFsrmCommittableCollection::Commit</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmderivedobjectsresult-get_derivedobjects">IFsrmDerivedObjectsResult::DerivedObjects</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmderivedobjectsresult-get_results">IFsrmDerivedObjectsResult::Results</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-enumactions">IFsrmFileScreenBase::EnumActions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition2-get_valuedefinitions">IFsrmPropertyDefinition2::ValueDefinitions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-enumthresholdactions">IFsrmQuotaBase::EnumThresholdActions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-enumreports">IFsrmReportJob::EnumReports</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-enumreportjobs">IFsrmReportManager::EnumReportJobs</a>
 

 

