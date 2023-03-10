---
UID: NF:fsrmreports.IFsrmReportManager.GetReportSizeLimit
title: IFsrmReportManager::GetReportSizeLimit (fsrmreports.h)
description: Retrieves the current value of the specified report size limit.
helpviewer_keywords: ["FsrmReportManager class [File Server Resource Manager]","GetReportSizeLimit method","GetReportSizeLimit","GetReportSizeLimit method [File Server Resource Manager]","GetReportSizeLimit method [File Server Resource Manager]","FsrmReportManager class","GetReportSizeLimit method [File Server Resource Manager]","IFsrmReportManager interface","IFsrmReportManager interface [File Server Resource Manager]","GetReportSizeLimit method","IFsrmReportManager.GetReportSizeLimit","IFsrmReportManager::GetReportSizeLimit","fs.ifsrmreportmanager_getreportsizelimit","fsrm.ifsrmreportmanager_getreportsizelimit","fsrmreports/IFsrmReportManager::GetReportSizeLimit"]
old-location: fsrm\ifsrmreportmanager_getreportsizelimit.htm
tech.root: fsrm
ms.assetid: 1fe2546c-d70c-466a-8640-77cc2403a91d
ms.date: 12/05/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],GetReportSizeLimit method, GetReportSizeLimit, GetReportSizeLimit method [File Server Resource Manager], GetReportSizeLimit method [File Server Resource Manager],FsrmReportManager class, GetReportSizeLimit method [File Server Resource Manager],IFsrmReportManager interface, IFsrmReportManager interface [File Server Resource Manager],GetReportSizeLimit method, IFsrmReportManager.GetReportSizeLimit, IFsrmReportManager::GetReportSizeLimit, fs.ifsrmreportmanager_getreportsizelimit, fsrm.ifsrmreportmanager_getreportsizelimit, fsrmreports/IFsrmReportManager::GetReportSizeLimit
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
 - IFsrmReportManager::GetReportSizeLimit
 - fsrmreports/IFsrmReportManager::GetReportSizeLimit
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
 - IFsrmReportManager.GetReportSizeLimit
 - FsrmReportManager.GetReportSizeLimit
---

# IFsrmReportManager::GetReportSizeLimit


## -description

Retrieves the current value of the specified report size limit.

## -parameters

### -param limit [in]

The report size limit which is used to limit the files listed in a report. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportlimit">FsrmReportLimit</a> enumeration.

### -param limitValue [out]

The limit. The variant type is <b>VT_I4</b>. Use the <b>lVal</b> member of the variant to access the limit value.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportmanager">IFsrmReportManager</a>