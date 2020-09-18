---
UID: NF:fsrmreports.IFsrmReportManager.GetDefaultFilter
title: IFsrmReportManager::GetDefaultFilter (fsrmreports.h)
description: Retrieves the default report filter value that is used with the specified report type.
helpviewer_keywords: ["FsrmReportManager class [File Server Resource Manager]","GetDefaultFilter method","GetDefaultFilter","GetDefaultFilter method [File Server Resource Manager]","GetDefaultFilter method [File Server Resource Manager]","FsrmReportManager class","GetDefaultFilter method [File Server Resource Manager]","IFsrmReportManager interface","IFsrmReportManager interface [File Server Resource Manager]","GetDefaultFilter method","IFsrmReportManager.GetDefaultFilter","IFsrmReportManager::GetDefaultFilter","fs.ifsrmreportmanager_getdefaultfilter","fsrm.ifsrmreportmanager_getdefaultfilter","fsrmreports/IFsrmReportManager::GetDefaultFilter"]
old-location: fsrm\ifsrmreportmanager_getdefaultfilter.htm
tech.root: fsrm
ms.assetid: 5f3a587e-c3a8-47ee-80ac-afa0824a4585
ms.date: 12/05/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],GetDefaultFilter method, GetDefaultFilter, GetDefaultFilter method [File Server Resource Manager], GetDefaultFilter method [File Server Resource Manager],FsrmReportManager class, GetDefaultFilter method [File Server Resource Manager],IFsrmReportManager interface, IFsrmReportManager interface [File Server Resource Manager],GetDefaultFilter method, IFsrmReportManager.GetDefaultFilter, IFsrmReportManager::GetDefaultFilter, fs.ifsrmreportmanager_getdefaultfilter, fsrm.ifsrmreportmanager_getdefaultfilter, fsrmreports/IFsrmReportManager::GetDefaultFilter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReportManager::GetDefaultFilter
 - fsrmreports/IFsrmReportManager::GetDefaultFilter
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
 - IFsrmReportManager.GetDefaultFilter
 - FsrmReportManager.GetDefaultFilter
---

# IFsrmReportManager::GetDefaultFilter


## -description

Retrieves the default report filter value that is used with the specified report type.

## -parameters

### -param reportType [in]

Report type. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreporttype">FsrmReportType</a> enumeration.

### -param filter [in]

Report filter. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportfilter">FsrmReportFilter</a> enumeration.

### -param filterValue [out]

The default report filter value.

## -returns

The method returns the following return values.

## -remarks

This value is used if the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreport-setfilter">IFsrmReport::SetFilter</a> method was not called to specify a filter value for the report.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportmanager">IFsrmReportManager</a>