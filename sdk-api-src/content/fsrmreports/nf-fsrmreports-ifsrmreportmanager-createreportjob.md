---
UID: NF:fsrmreports.IFsrmReportManager.CreateReportJob
title: IFsrmReportManager::CreateReportJob
author: windows-sdk-content
description: Creates a report job.
old-location: fsrm\ifsrmreportmanager_createreportjob.htm
old-project: Fsrm
ms.assetid: 30274108-a820-409e-ba7c-6971b7726b9b
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: CreateReportJob, CreateReportJob method [File Server Resource Manager], CreateReportJob method [File Server Resource Manager],FsrmReportManager class, CreateReportJob method [File Server Resource Manager],IFsrmReportManager interface, FsrmReportManager class [File Server Resource Manager],CreateReportJob method, IFsrmReportManager interface [File Server Resource Manager],CreateReportJob method, IFsrmReportManager.CreateReportJob, IFsrmReportManager::CreateReportJob, fs.ifsrmreportmanager_createreportjob, fsrm.ifsrmreportmanager_createreportjob, fsrmreports/IFsrmReportManager::CreateReportJob
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmReportManager.CreateReportJob
-	FsrmReportManager.CreateReportJob
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportManager::CreateReportJob


## -description


Creates a report job.


## -parameters




### -param reportJob [out]

An <a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a> interface of the newly created 
      report job object. Use the interface to add reports to the job and run the reports. To add the report job to 
      FSRM, call <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmReportJob::Commit</a> method.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

