---
UID: NE:fsrmenums._FsrmReportFormat
title: FsrmReportFormat (fsrmenums.h)
description: Defines the file formats that you can use when generating reports.
helpviewer_keywords: ["FsrmReportFormat","FsrmReportFormat enumeration [File Server Resource Manager]","FsrmReportFormat_Csv","FsrmReportFormat_DHtml","FsrmReportFormat_Html","FsrmReportFormat_Txt","FsrmReportFormat_Unknown","FsrmReportFormat_Xml","fs.fsrmreportformat","fsrm.fsrmreportformat","fsrmenums/FsrmReportFormat","fsrmenums/FsrmReportFormat_Csv","fsrmenums/FsrmReportFormat_DHtml","fsrmenums/FsrmReportFormat_Html","fsrmenums/FsrmReportFormat_Txt","fsrmenums/FsrmReportFormat_Unknown","fsrmenums/FsrmReportFormat_Xml"]
old-location: fsrm\fsrmreportformat.htm
tech.root: fsrm
ms.assetid: 0f8fd733-034a-40d0-b59b-4c70fff5fd42
ms.date: 12/05/2018
ms.keywords: FsrmReportFormat, FsrmReportFormat enumeration [File Server Resource Manager], FsrmReportFormat_Csv, FsrmReportFormat_DHtml, FsrmReportFormat_Html, FsrmReportFormat_Txt, FsrmReportFormat_Unknown, FsrmReportFormat_Xml, fs.fsrmreportformat, fsrm.fsrmreportformat, fsrmenums/FsrmReportFormat, fsrmenums/FsrmReportFormat_Csv, fsrmenums/FsrmReportFormat_DHtml, fsrmenums/FsrmReportFormat_Html, fsrmenums/FsrmReportFormat_Txt, fsrmenums/FsrmReportFormat_Unknown, fsrmenums/FsrmReportFormat_Xml
req.header: fsrmenums.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FsrmReportFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmReportFormat
 - fsrmenums/_FsrmReportFormat
 - FsrmReportFormat
 - fsrmenums/FsrmReportFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmReportFormat
---

# FsrmReportFormat enumeration


## -description

Defines the file formats that you can use when generating reports.

## -enum-fields

### -field FsrmReportFormat_Unknown:0

The report format is unknown. Do not use this flag.

### -field FsrmReportFormat_DHtml:1

The report is rendered in Dynamic HTML (DHTML).

### -field FsrmReportFormat_Html:2

The report is rendered in HTML.

### -field FsrmReportFormat_Txt:3

The report is rendered as a text file.

### -field FsrmReportFormat_Csv:4

The report is rendered as a comma-separated value file.

### -field FsrmReportFormat_Xml:5

The report is rendered in XML.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_formats">IFsrmReportJob::Formats</a>
