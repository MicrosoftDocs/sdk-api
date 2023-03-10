---
UID: NF:fsrmreports.IFsrmReport.Delete
title: IFsrmReport::Delete (fsrmreports.h)
description: Removes this report object from the report job object.
helpviewer_keywords: ["Delete","Delete method [File Server Resource Manager]","Delete method [File Server Resource Manager]","IFsrmReport interface","IFsrmReport interface [File Server Resource Manager]","Delete method","IFsrmReport.Delete","IFsrmReport::Delete","fs.ifsrmreport_delete","fsrm.ifsrmreport_delete","fsrmreports/IFsrmReport::Delete"]
old-location: fsrm\ifsrmreport_delete.htm
tech.root: fsrm
ms.assetid: b50139bc-c584-4bed-bf2e-34f1fef16e6d
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [File Server Resource Manager], Delete method [File Server Resource Manager],IFsrmReport interface, IFsrmReport interface [File Server Resource Manager],Delete method, IFsrmReport.Delete, IFsrmReport::Delete, fs.ifsrmreport_delete, fsrm.ifsrmreport_delete, fsrmreports/IFsrmReport::Delete
req.header: fsrmreports.h
req.include-header: 
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
 - IFsrmReport::Delete
 - fsrmreports/IFsrmReport::Delete
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
 - IFsrmReport.Delete
---

# IFsrmReport::Delete


## -description

Removes this report object from the report job object.



## -returns

The method returns the following return values.

## -remarks

Note that the reports are not deleted until you call the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmReportJob::Commit</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreport">IFsrmReport</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a>
