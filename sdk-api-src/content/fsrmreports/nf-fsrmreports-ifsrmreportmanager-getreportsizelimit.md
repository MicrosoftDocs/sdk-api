---
UID: NF:fsrmreports.IFsrmReportManager.GetReportSizeLimit
title: IFsrmReportManager::GetReportSizeLimit
author: windows-sdk-content
description: Retrieves the current value of the specified report size limit.
old-location: fsrm\ifsrmreportmanager_getreportsizelimit.htm
tech.root: Fsrm
ms.assetid: 1fe2546c-d70c-466a-8640-77cc2403a91d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],GetReportSizeLimit method, GetReportSizeLimit, GetReportSizeLimit method [File Server Resource Manager], GetReportSizeLimit method [File Server Resource Manager],FsrmReportManager class, GetReportSizeLimit method [File Server Resource Manager],IFsrmReportManager interface, IFsrmReportManager interface [File Server Resource Manager],GetReportSizeLimit method, IFsrmReportManager.GetReportSizeLimit, IFsrmReportManager::GetReportSizeLimit, fs.ifsrmreportmanager_getreportsizelimit, fsrm.ifsrmreportmanager_getreportsizelimit, fsrmreports/IFsrmReportManager::GetReportSizeLimit
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
 - IFsrmReportManager.GetReportSizeLimit
 - FsrmReportManager.GetReportSizeLimit
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
- IFsrmReportManager.GetReportSizeLimit
: 
---

# IFsrmReportManager::GetReportSizeLimit


## -description


Retrieves the current value of the specified report size limit.


## -parameters




### -param limit [in]

The report size limit which is used to limit the files listed in a report. For possible values, see the <a href="https://msdn.microsoft.com/225c583c-679c-43b4-85f4-3f2294fa7bc3">FsrmReportLimit</a> enumeration.


### -param limitValue [out]

The limit. The variant type is <b>VT_I4</b>. Use the <b>lVal</b> member of the variant to access the limit value.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

