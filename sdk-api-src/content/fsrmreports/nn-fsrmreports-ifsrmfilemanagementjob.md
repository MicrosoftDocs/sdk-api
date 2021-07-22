---
UID: NN:fsrmreports.IFsrmFileManagementJob
title: IFsrmFileManagementJob (fsrmreports.h)
description: Defines a file management job.
helpviewer_keywords: ["IFsrmFileManagementJob","IFsrmFileManagementJob interface [File Server Resource Manager]","IFsrmFileManagementJob interface [File Server Resource Manager]","described","fs.ifsrmfilemanagementjob","fsrm.ifsrmfilemanagementjob","fsrm/IFsrmFileManagementJob"]
old-location: fsrm\ifsrmfilemanagementjob.htm
tech.root: fsrm
ms.assetid: e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob, IFsrmFileManagementJob interface [File Server Resource Manager], IFsrmFileManagementJob interface [File Server Resource Manager],described, fs.ifsrmfilemanagementjob, fsrm.ifsrmfilemanagementjob, fsrm/IFsrmFileManagementJob
req.header: fsrmreports.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - IFsrmFileManagementJob
 - fsrmreports/IFsrmFileManagementJob
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
 - IFsrmFileManagementJob
---

# IFsrmFileManagementJob interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Defines a file management job. The job specifies a schedule, conditions, a command or 
    actions to execute if a file meets all the conditions, user notifications, and reporting.

To create a file management job, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-createfilemanagementjob">IFsrmFileManagementJobManager::CreateFileManagementJob</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-enumfilemanagementjobs">IFsrmFileManagementJobManager::EnumFileManagementJobs</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-getfilemanagementjob">IFsrmFileManagementJobManager::GetFileManagementJob</a>
</li>
</ul>If a file management job object is modified using 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> or a related WMI 
    class, then the methods and properties of the 
    <b>IFsrmFileManagementJob</b> interface may no longer be 
    usable and fail in unexpected ways when working with the same job.

## -inheritance

The <b>IFsrmFileManagementJob</b> interface inherits from <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>. <b>IFsrmFileManagementJob</b> also has these types of members:

## -remarks

When a file management job runs, it scans the files in the specified folders and if a file in the folder meets 
    the conditions specified by the job, FSRM moves the file to the specified expired files folder if the type is 
    expiration, or runs the custom action if defined. If notifications or actions are specified, FSRM sends the 
    notifications and performs the actions.

Use the following properties to specify the expiration conditions:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilecreated">DaysSinceFileCreated</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilelastaccessed">DaysSinceFileLastAccessed</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_dayssincefilelastmodified">DaysSinceFileLastModified</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_propertyconditions">PropertyConditions</a> (use 
      the 
      <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createpropertycondition">CreatePropertyCondition</a> 
      method to create the property condition)</li>
</ul>
FSRM performs a logical AND on all the conditions to determine if the file meets those conditions.

FSRM does not expire files in the system directories (for example, "\Windows", 
    "\System Volume Information", "$Event", and 
    "$Recycle").

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
