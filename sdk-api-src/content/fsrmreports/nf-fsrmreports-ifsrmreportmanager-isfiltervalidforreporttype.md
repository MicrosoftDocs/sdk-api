---
UID: NF:fsrmreports.IFsrmReportManager.IsFilterValidForReportType
title: IFsrmReportManager::IsFilterValidForReportType method
author: windows-driver-content
description: Retrieves a value that determines whether a specified report filter is configurable for the specified report type.
old-location: fsrm\ifsrmreportmanager_isfiltervalidforreporttype.htm
old-project: Fsrm
ms.assetid: e9f93b97-c8ac-441a-9f6b-87d45bd10cdf
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager], IsFilterValidForReportType method, IFsrmReportManager, IFsrmReportManager interface [File Server Resource Manager], IsFilterValidForReportType method, IFsrmReportManager::IsFilterValidForReportType, IsFilterValidForReportType method [File Server Resource Manager], IsFilterValidForReportType method [File Server Resource Manager], FsrmReportManager class, IsFilterValidForReportType method [File Server Resource Manager], IFsrmReportManager interface, IsFilterValidForReportType,IFsrmReportManager.IsFilterValidForReportType, fs.ifsrmreportmanager_isfiltervalidforreporttype, fsrm.ifsrmreportmanager_isfiltervalidforreporttype, fsrmreports/IFsrmReportManager::IsFilterValidForReportType
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
-	IFsrmReportManager.IsFilterValidForReportType
-	FsrmReportManager.IsFilterValidForReportType
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportManager::IsFilterValidForReportType method


## -description


Retrieves a value that determines whether a specified report filter is configurable for the specified report type.


## -parameters




### -param reportType [in]

Report type. For possible values, see the <a href="https://msdn.microsoft.com/6fb5cb02-371b-4d07-9f13-d0409d5835d4">FsrmReportType</a> enumeration.


### -param filter [in]

Report filter. For possible values, see the <a href="https://msdn.microsoft.com/6f38ec9a-8876-44ce-9d44-f3982f1880ca">FsrmReportFilter</a> enumeration.


### -param valid [out]

Is <b>VARIANT_TRUE</b> if the filter is configurable for the report type, otherwise it is <b>VARIANT_FALSE</b>.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

