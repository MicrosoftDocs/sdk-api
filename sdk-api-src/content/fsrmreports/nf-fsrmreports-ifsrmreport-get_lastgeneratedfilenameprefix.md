---
UID: NF:fsrmreports.IFsrmReport.get_LastGeneratedFileNamePrefix
title: IFsrmReport::get_LastGeneratedFileNamePrefix (fsrmreports.h)
description: Retrieves the report's generated file name for the last time the report was run.
helpviewer_keywords: ["IFsrmReport interface [File Server Resource Manager]","LastGeneratedFileNamePrefix property","IFsrmReport.LastGeneratedFileNamePrefix","IFsrmReport.get_LastGeneratedFileNamePrefix","IFsrmReport::LastGeneratedFileNamePrefix","IFsrmReport::get_LastGeneratedFileNamePrefix","LastGeneratedFileNamePrefix property [File Server Resource Manager]","LastGeneratedFileNamePrefix property [File Server Resource Manager]","IFsrmReport interface","fs.ifsrmreport_lastgeneratedfilenameprefix","fsrm.ifsrmreport_lastgeneratedfilenameprefix","fsrmreports/IFsrmReport::LastGeneratedFileNamePrefix","fsrmreports/IFsrmReport::get_LastGeneratedFileNamePrefix","get_LastGeneratedFileNamePrefix"]
old-location: fsrm\ifsrmreport_lastgeneratedfilenameprefix.htm
tech.root: fsrm
ms.assetid: 7aff8040-5d67-42a0-89ba-028cf39bd40a
ms.date: 12/05/2018
ms.keywords: IFsrmReport interface [File Server Resource Manager],LastGeneratedFileNamePrefix property, IFsrmReport.LastGeneratedFileNamePrefix, IFsrmReport.get_LastGeneratedFileNamePrefix, IFsrmReport::LastGeneratedFileNamePrefix, IFsrmReport::get_LastGeneratedFileNamePrefix, LastGeneratedFileNamePrefix property [File Server Resource Manager], LastGeneratedFileNamePrefix property [File Server Resource Manager],IFsrmReport interface, fs.ifsrmreport_lastgeneratedfilenameprefix, fsrm.ifsrmreport_lastgeneratedfilenameprefix, fsrmreports/IFsrmReport::LastGeneratedFileNamePrefix, fsrmreports/IFsrmReport::get_LastGeneratedFileNamePrefix, get_LastGeneratedFileNamePrefix
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
 - IFsrmReport::get_LastGeneratedFileNamePrefix
 - fsrmreports/IFsrmReport::get_LastGeneratedFileNamePrefix
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
 - IFsrmReport.LastGeneratedFileNamePrefix
 - IFsrmReport.get_LastGeneratedFileNamePrefix
---

# IFsrmReport::get_LastGeneratedFileNamePrefix


## -description

Retrieves the report's generated file name for the last time the report was run. The string is used to make the report name unique.

This property is read-only.

## -parameters

## -remarks

The file names are generated to identify the collection of files that were generated for a report job the last time the report job ran.

To determine where the reports are stored, access the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_lastgeneratedindirectory">IFsrmReportJob::LastGeneratedInDirectory</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreport">IFsrmReport</a>