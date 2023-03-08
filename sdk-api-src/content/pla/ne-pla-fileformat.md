---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0002
title: FileFormat (pla.h)
description: Defines the format of the data in the log file.
helpviewer_keywords: ["FileFormat","FileFormat enumeration [PLA]","base.fileformat","pla.fileformat","pla/FileFormat","pla/plaBinary","pla/plaCommaSeparated","pla/plaSql","pla/plaTabSeparated","plaBinary","plaCommaSeparated","plaSql","plaTabSeparated"]
old-location: pla\fileformat.htm
tech.root: PLA
ms.assetid: 8ec50a96-0c8c-401a-8849-e3753fe15952
ms.date: 12/05/2018
ms.keywords: FileFormat, FileFormat enumeration [PLA], base.fileformat, pla.fileformat, pla/FileFormat, pla/plaBinary, pla/plaCommaSeparated, pla/plaSql, pla/plaTabSeparated, plaBinary, plaCommaSeparated, plaSql, plaTabSeparated
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FileFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_pla_0001_0043_0002
 - pla/__MIDL___MIDL_itf_pla_0001_0043_0002
 - FileFormat
 - pla/FileFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - FileFormat
---

# FileFormat enumeration


## -description

Defines the format of the data in the log file.

## -enum-fields

### -field plaCommaSeparated:0

Comma-separated log file. The first line in the text file contains column headings followed by comma-separated data in the remaining lines of the log file.

### -field plaTabSeparated:1

Tab-separated log file. The first line in the text file contains column headings followed by tab-separated data in the remaining lines of the log file.

### -field plaSql:2

The log contains SQL records.

### -field plaBinary:3

Binary log file.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-iperformancecounterdatacollector-get_logfileformat">IPerformanceCounterDataCollector::LogFileFormat</a>
