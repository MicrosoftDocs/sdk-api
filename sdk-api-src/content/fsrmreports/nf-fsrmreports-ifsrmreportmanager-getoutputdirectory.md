---
UID: NF:fsrmreports.IFsrmReportManager.GetOutputDirectory
title: IFsrmReportManager::GetOutputDirectory
author: windows-sdk-content
description: Retrieves the local directory path where the reports with the specified context are stored.
old-location: fsrm\ifsrmreportmanager_getoutputdirectory.htm
old-project: Fsrm
ms.assetid: 90df1a6e-e2e6-4095-8337-61bfd172e203
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],GetOutputDirectory method, GetOutputDirectory, GetOutputDirectory method [File Server Resource Manager], GetOutputDirectory method [File Server Resource Manager],FsrmReportManager class, GetOutputDirectory method [File Server Resource Manager],IFsrmReportManager interface, IFsrmReportManager interface [File Server Resource Manager],GetOutputDirectory method, IFsrmReportManager.GetOutputDirectory, IFsrmReportManager::GetOutputDirectory, fs.ifsrmreportmanager_getoutputdirectory, fsrm.ifsrmreportmanager_getoutputdirectory, fsrmreports/IFsrmReportManager::GetOutputDirectory
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
-	IFsrmReportManager.GetOutputDirectory
-	FsrmReportManager.GetOutputDirectory
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportManager::GetOutputDirectory


## -description


Retrieves the local directory path where the reports with the specified context are stored.


## -parameters




### -param context [in]

The report context (for example, if the report is scheduled or run on demand). For possible values, see the <a href="https://msdn.microsoft.com/02e18cc2-7c5e-473f-8a7f-e310bfb1c57d">FsrmReportGenerationContext</a> enumeration.


### -param path [out]

The local directory path where the reports are stored.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

