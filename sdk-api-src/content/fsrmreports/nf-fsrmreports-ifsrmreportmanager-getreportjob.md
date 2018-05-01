---
UID: NF:fsrmreports.IFsrmReportManager.GetReportJob
title: IFsrmReportManager::GetReportJob method
author: windows-driver-content
description: Retrieves the specified report job.
old-location: fsrm\ifsrmreportmanager_getreportjob.htm
old-project: Fsrm
ms.assetid: 60a1387f-a25f-4026-a582-71981c26dd1b
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager], GetReportJob method, GetReportJob method [File Server Resource Manager], GetReportJob method [File Server Resource Manager], FsrmReportManager class, GetReportJob method [File Server Resource Manager], IFsrmReportManager interface, GetReportJob,IFsrmReportManager.GetReportJob, IFsrmReportManager, IFsrmReportManager interface [File Server Resource Manager], GetReportJob method, IFsrmReportManager::GetReportJob, fs.ifsrmreportmanager_getreportjob, fsrm.ifsrmreportmanager_getreportjob, fsrmreports/IFsrmReportManager::GetReportJob
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmReportManager.GetReportJob
-	FsrmReportManager.GetReportJob
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportManager::GetReportJob method


## -description


Retrieves the specified report job.


## -parameters




### -param taskName [in]

The task name that identifies the report job to retrieve. The string is limited to 230 characters.


### -param reportJob [out]

An <a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a> interface to the retrieved job.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

