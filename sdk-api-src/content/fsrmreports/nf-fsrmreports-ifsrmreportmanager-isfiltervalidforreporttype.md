---
UID: NF:fsrmreports.IFsrmReportManager.IsFilterValidForReportType
title: IFsrmReportManager::IsFilterValidForReportType (fsrmreports.h)
description: Retrieves a value that determines whether a specified report filter is configurable for the specified report type.
old-location: fsrm\ifsrmreportmanager_isfiltervalidforreporttype.htm
tech.root: fsrm
ms.assetid: e9f93b97-c8ac-441a-9f6b-87d45bd10cdf
ms.date: 12/05/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],IsFilterValidForReportType method, IFsrmReportManager interface [File Server Resource Manager],IsFilterValidForReportType method, IFsrmReportManager.IsFilterValidForReportType, IFsrmReportManager::IsFilterValidForReportType, IsFilterValidForReportType, IsFilterValidForReportType method [File Server Resource Manager], IsFilterValidForReportType method [File Server Resource Manager],FsrmReportManager class, IsFilterValidForReportType method [File Server Resource Manager],IFsrmReportManager interface, fs.ifsrmreportmanager_isfiltervalidforreporttype, fsrm.ifsrmreportmanager_isfiltervalidforreporttype, fsrmreports/IFsrmReportManager::IsFilterValidForReportType
f1_keywords:
- fsrmreports/IFsrmReportManager.IsFilterValidForReportType
dev_langs:
- c++
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
- IFsrmReportManager.IsFilterValidForReportType
- FsrmReportManager.IsFilterValidForReportType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmReportManager::IsFilterValidForReportType


## -description


Retrieves a value that determines whether a specified report filter is configurable for the specified report type.


## -parameters




### -param reportType [in]

Report type. For possible values, see the <a href="https://docs.microsoft.com/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreporttype">FsrmReportType</a> enumeration.


### -param filter [in]

Report filter. For possible values, see the <a href="https://docs.microsoft.com/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportfilter">FsrmReportFilter</a> enumeration.


### -param valid [out]

Is <b>VARIANT_TRUE</b> if the filter is configurable for the report type, otherwise it is <b>VARIANT_FALSE</b>.


## -returns



The method returns the following return values.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportmanager">IFsrmReportManager</a>
 

 

