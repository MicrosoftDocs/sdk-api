---
UID: NF:pla.IDataCollector.get_FileName
title: IDataCollector::get_FileName (pla.h)
description: Retrieves or sets the base name of the file that will contain the data collector data. (Get)
helpviewer_keywords: ["FileName property [PLA]","FileName property [PLA]","IDataCollector interface","IDataCollector interface [PLA]","FileName property","IDataCollector.FileName","IDataCollector.get_FileName","IDataCollector::FileName","IDataCollector::get_FileName","IDataCollector::put_FileName","base.idatacollector_filename","get_FileName","pla.idatacollector_filename","pla/IDataCollector::FileName","pla/IDataCollector::get_FileName","pla/IDataCollector::put_FileName"]
old-location: pla\idatacollector_filename.htm
tech.root: PLA
ms.assetid: 9208baf8-0bc7-45c4-a912-7b59f4c1ca6a
ms.date: 12/05/2018
ms.keywords: FileName property [PLA], FileName property [PLA],IDataCollector interface, IDataCollector interface [PLA],FileName property, IDataCollector.FileName, IDataCollector.get_FileName, IDataCollector::FileName, IDataCollector::get_FileName, IDataCollector::put_FileName, base.idatacollector_filename, get_FileName, pla.idatacollector_filename, pla/IDataCollector::FileName, pla/IDataCollector::get_FileName, pla/IDataCollector::put_FileName
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataCollector::get_FileName
 - pla/IDataCollector::get_FileName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollector.FileName
 - IDataCollector.get_FileName
 - IDataCollector.put_FileName
---

# IDataCollector::get_FileName


## -description

Retrieves or sets the base name of the file that will contain the data collector data.

This property is read/write.

## -parameters

## -remarks

The actual file name used could be different if you specified formatting options in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformat">IDataCollector::FileNameFormat</a> property. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_latestoutputlocation">IDataCollector::LatestOutputLocation</a> property contains the actual file name used. 

Do not include the path in the file name; the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">IDataCollectorSet::RootPath</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectory">IDataCollectorSet::Subdirectory</a> properties determine the path to the file.

The file name extension that you specify depends on the type of data collector. The following table shows the correct extension to use for each data collector. If you specify a different extension, PLA will use it. If you do not specify an extension, PLA adds the correct extension to the file. 

<table>
<tr>
<th>Data collector type</th>
<th>Extension to use</th>
</tr>
<tr>
<td>Configuration data collectors</td>
<td>.xml</td>
</tr>
<tr>
<td>Performance data collectors</td>
<td>Can be .blg, .csv, or .tsv depending on the value of the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-iperformancecounterdatacollector-get_logfileformat">IPerformanceCounterDataCollector::LogFileFormat</a> property. </td>
</tr>
<tr>
<td>Trace data collectors</td>
<td>.etl</td>
</tr>
</table>
 

The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logappend">IDataCollector::LogAppend</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logoverwrite">IDataCollector::LogOverwrite</a> properties determine the action taken if the file already exists.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformat">IDataCollector::FileNameFormat</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformatpattern">IDataCollector::FileNameFormatPattern</a>
