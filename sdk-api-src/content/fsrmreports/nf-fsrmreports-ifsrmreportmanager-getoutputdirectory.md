---
UID: NF:fsrmreports.IFsrmReportManager.GetOutputDirectory
title: IFsrmReportManager::GetOutputDirectory (fsrmreports.h)
description: Retrieves the local directory path where the reports with the specified context are stored.
helpviewer_keywords: ["FsrmReportManager class [File Server Resource Manager]","GetOutputDirectory method","GetOutputDirectory","GetOutputDirectory method [File Server Resource Manager]","GetOutputDirectory method [File Server Resource Manager]","FsrmReportManager class","GetOutputDirectory method [File Server Resource Manager]","IFsrmReportManager interface","IFsrmReportManager interface [File Server Resource Manager]","GetOutputDirectory method","IFsrmReportManager.GetOutputDirectory","IFsrmReportManager::GetOutputDirectory","fs.ifsrmreportmanager_getoutputdirectory","fsrm.ifsrmreportmanager_getoutputdirectory","fsrmreports/IFsrmReportManager::GetOutputDirectory"]
old-location: fsrm\ifsrmreportmanager_getoutputdirectory.htm
tech.root: fsrm
ms.assetid: 90df1a6e-e2e6-4095-8337-61bfd172e203
ms.date: 12/05/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],GetOutputDirectory method, GetOutputDirectory, GetOutputDirectory method [File Server Resource Manager], GetOutputDirectory method [File Server Resource Manager],FsrmReportManager class, GetOutputDirectory method [File Server Resource Manager],IFsrmReportManager interface, IFsrmReportManager interface [File Server Resource Manager],GetOutputDirectory method, IFsrmReportManager.GetOutputDirectory, IFsrmReportManager::GetOutputDirectory, fs.ifsrmreportmanager_getoutputdirectory, fsrm.ifsrmreportmanager_getoutputdirectory, fsrmreports/IFsrmReportManager::GetOutputDirectory
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
 - IFsrmReportManager::GetOutputDirectory
 - fsrmreports/IFsrmReportManager::GetOutputDirectory
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
 - IFsrmReportManager.GetOutputDirectory
 - FsrmReportManager.GetOutputDirectory
---

# IFsrmReportManager::GetOutputDirectory


## -description

Retrieves the local directory path where the reports with the specified context are stored.

## -parameters

### -param context [in]

The report context (for example, if the report is scheduled or run on demand). For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportgenerationcontext">FsrmReportGenerationContext</a> enumeration.

### -param path [out]

The local directory path where the reports are stored.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportmanager">IFsrmReportManager</a>