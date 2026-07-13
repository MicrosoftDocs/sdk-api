---
UID: NN:fsrm.IFsrmCollection
title: IFsrmCollection (fsrm.h)
description: Defines a collection of FSRM objects.
helpviewer_keywords: ["IFsrmCollection","IFsrmCollection interface [File Server Resource Manager]","IFsrmCollection interface [File Server Resource Manager]","described","fs.ifsrmcollection","fsrm.ifsrmcollection","fsrm/IFsrmCollection"]
old-location: fsrm\ifsrmcollection.htm
tech.root: fsrm
ms.assetid: 6a0c5d8b-5fed-4c55-971c-43430e3c6a8d
ms.date: 12/05/2018
ms.keywords: IFsrmCollection, IFsrmCollection interface [File Server Resource Manager], IFsrmCollection interface [File Server Resource Manager],described, fs.ifsrmcollection, fsrm.ifsrmcollection, fsrm/IFsrmCollection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmCollection
 - fsrm/IFsrmCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmCollection
---

# IFsrmCollection interface


## -description

Defines a collection of FSRM objects.

The following methods and properties return this collection:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcommittablecollection-commit">IFsrmCommittableCollection::Commit</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmderivedobjectsresult-get_derivedobjects">IFsrmDerivedObjectsResult::DerivedObjects</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmderivedobjectsresult-get_results">IFsrmDerivedObjectsResult::Results</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-enumactions">IFsrmFileScreenBase::EnumActions</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition2-get_valuedefinitions">IFsrmPropertyDefinition2::ValueDefinitions</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-enumthresholdactions">IFsrmQuotaBase::EnumThresholdActions</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-enumreports">IFsrmReportJob::EnumReports</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-enumreportjobs">IFsrmReportManager::EnumReportJobs</a>
</li>
</ul>The collection is empty if the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-get_count">Count</a> property is 
    zero.

## -inheritance

The <b>IFsrmCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmCollection</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcommittablecollection-commit">IFsrmCommittableCollection::Commit</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmderivedobjectsresult-get_derivedobjects">IFsrmDerivedObjectsResult::DerivedObjects</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmderivedobjectsresult-get_results">IFsrmDerivedObjectsResult::Results</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-enumactions">IFsrmFileScreenBase::EnumActions</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition2-get_valuedefinitions">IFsrmPropertyDefinition2::ValueDefinitions</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-enumthresholdactions">IFsrmQuotaBase::EnumThresholdActions</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-enumreports">IFsrmReportJob::EnumReports</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-enumreportjobs">IFsrmReportManager::EnumReportJobs</a>
