---
UID: NF:fsrmreports.IFsrmReportManager.GetDefaultFilter
title: IFsrmReportManager::GetDefaultFilter
author: windows-sdk-content
description: Retrieves the default report filter value that is used with the specified report type.
old-location: fsrm\ifsrmreportmanager_getdefaultfilter.htm
tech.root: Fsrm
ms.assetid: 5f3a587e-c3a8-47ee-80ac-afa0824a4585
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],GetDefaultFilter method, GetDefaultFilter, GetDefaultFilter method [File Server Resource Manager], GetDefaultFilter method [File Server Resource Manager],FsrmReportManager class, GetDefaultFilter method [File Server Resource Manager],IFsrmReportManager interface, IFsrmReportManager interface [File Server Resource Manager],GetDefaultFilter method, IFsrmReportManager.GetDefaultFilter, IFsrmReportManager::GetDefaultFilter, fs.ifsrmreportmanager_getdefaultfilter, fsrm.ifsrmreportmanager_getdefaultfilter, fsrmreports/IFsrmReportManager::GetDefaultFilter
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
 - IFsrmReportManager.GetDefaultFilter
 - FsrmReportManager.GetDefaultFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmreports.h
: 
- IFsrmReportManager.GetDefaultFilter
: 
---

# IFsrmReportManager::GetDefaultFilter


## -description


Retrieves the default report filter value that is used with the specified report type.


## -parameters




### -param reportType [in]

Report type. For possible values, see the <a href="https://msdn.microsoft.com/6fb5cb02-371b-4d07-9f13-d0409d5835d4">FsrmReportType</a> enumeration.


### -param filter [in]

Report filter. For possible values, see the <a href="https://msdn.microsoft.com/6f38ec9a-8876-44ce-9d44-f3982f1880ca">FsrmReportFilter</a> enumeration.


### -param filterValue [out]

The default report filter value.


## -returns



The method returns the following return values.




## -remarks



This value is used if the <a href="https://msdn.microsoft.com/6d36e3e2-7826-4bae-943c-3ab73404534c">IFsrmReport::SetFilter</a> method was not called to specify a filter value for the report.




## -see-also




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

