---
UID: NN:fsrmreports.IFsrmReport
title: IFsrmReport (fsrmreports.h)
description: Used to configure the description and filters for a single report.
helpviewer_keywords: ["IFsrmReport","IFsrmReport interface [File Server Resource Manager]","IFsrmReport interface [File Server Resource Manager]","described","fs.ifsrmreport","fsrm.ifsrmreport","fsrm/IFsrmReport"]
old-location: fsrm\ifsrmreport.htm
tech.root: fsrm
ms.assetid: 2172a543-b3b7-453e-887b-05c8ee74f197
ms.date: 12/05/2018
ms.keywords: IFsrmReport, IFsrmReport interface [File Server Resource Manager], IFsrmReport interface [File Server Resource Manager],described, fs.ifsrmreport, fsrm.ifsrmreport, fsrm/IFsrmReport
req.header: fsrmreports.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmReport
 - fsrmreports/IFsrmReport
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
 - IFsrmReport
---

# IFsrmReport interface


## -description

Used to configure the description and filters for a single report.

To create this interface, call the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-createreport">IFsrmReportJob::CreateReport</a> method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-enumreports">IFsrmReportJob::EnumReports</a>
</li>
</ul>

## -inheritance

The <b>IFsrmReport</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmReport</b> also has these types of members:

