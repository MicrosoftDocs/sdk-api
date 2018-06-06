---
UID: NF:fsrmreports.IFsrmReportManager.EnumReportJobs
title: IFsrmReportManager::EnumReportJobs
author: windows-sdk-content
description: Enumerates the report jobs.
old-location: fsrm\ifsrmreportmanager_enumreportjobs.htm
old-project: Fsrm
ms.assetid: af66beb6-e82c-47e6-8658-da9702041053
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: EnumReportJobs, EnumReportJobs method [File Server Resource Manager], EnumReportJobs method [File Server Resource Manager],FsrmReportManager class, EnumReportJobs method [File Server Resource Manager],IFsrmReportManager interface, FsrmReportManager class [File Server Resource Manager],EnumReportJobs method, IFsrmReportManager interface [File Server Resource Manager],EnumReportJobs method, IFsrmReportManager.EnumReportJobs, IFsrmReportManager::EnumReportJobs, fs.ifsrmreportmanager_enumreportjobs, fsrm.ifsrmreportmanager_enumreportjobs, fsrmreports/IFsrmReportManager::EnumReportJobs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmreports.h
req.include-header: FsrmReports.h, FsrmTlb.h
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReportManager.EnumReportJobs
 - FsrmReportManager.EnumReportJobs
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportManager::EnumReportJobs


## -description


Enumerates the report jobs.


## -parameters




### -param options [in]

The options to use when enumerating the report jobs. For possible values, see the 
      <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.

<div class="alert"><b>Note</b>  The <b>FsrmEnumOptions_Asynchronous</b> option is not supported for this 
       method.</div>
<div> </div>

### -param reportJobs [out]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a 
      collection of the report jobs. The collection is empty if no report jobs.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member to get the 
       <a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a> interface.

The collection can contain committed and uncommitted report jobs. For an uncommitted report job to be 
       included in the collection, the running status of the job must be 
       <b>FsrmReportRunningStatus_Queued</b> or 
       <b>FsrmReportRunningStatus_Running</b>.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

