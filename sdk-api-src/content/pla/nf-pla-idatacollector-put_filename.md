---
UID: NF:pla.IDataCollector.put_FileName
title: IDataCollector::put_FileName
author: windows-sdk-content
description: Retrieves or sets the base name of the file that will contain the data collector data.
old-location: pla\idatacollector_filename.htm
old-project: PLA
ms.assetid: 9208baf8-0bc7-45c4-a912-7b59f4c1ca6a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: FileName property [PLA], FileName property [PLA],IDataCollector interface, IDataCollector interface [PLA],FileName property, IDataCollector.FileName, IDataCollector.put_FileName, IDataCollector::FileName, IDataCollector::get_FileName, IDataCollector::put_FileName, base.idatacollector_filename, pla.idatacollector_filename, pla/IDataCollector::FileName, pla/IDataCollector::get_FileName, pla/IDataCollector::put_FileName, put_FileName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FolderActionSteps
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
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IDataCollector::put_FileName


## -description


Retrieves or sets the base name of the file that will contain the data collector data.

This property is read/write.


## -parameters


## -remarks



The actual file name used could be different if you specified formatting options in the <a href="https://msdn.microsoft.com/3a7744a6-feb3-4aea-856d-8496aecc0176">IDataCollector::FileNameFormat</a> property. The <a href="https://msdn.microsoft.com/e451c3a7-aec3-4fa7-9313-730bfac55f19">IDataCollector::LatestOutputLocation</a> property contains the actual file name used. 

Do not include the path in the file name; the <a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">IDataCollectorSet::RootPath</a> and <a href="https://msdn.microsoft.com/c2c55fd9-3b29-46be-9792-acb095b1c0e4">IDataCollectorSet::Subdirectory</a> properties determine the path to the file.

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
<td>Can be .blg, .csv, or .tsv depending on the value of the <a href="https://msdn.microsoft.com/3b980ea6-cb08-4e10-b4b3-40fd504d5e8f">IPerformanceCounterDataCollector::LogFileFormat</a> property. </td>
</tr>
<tr>
<td>Trace data collectors</td>
<td>.etl</td>
</tr>
</table>
 

The <a href="https://msdn.microsoft.com/c9843647-2c36-4d08-98d0-4df63b054993">IDataCollector::LogAppend</a> and <a href="https://msdn.microsoft.com/17f40639-2e24-4a7e-b934-036d8595bdbf">IDataCollector::LogOverwrite</a> properties determine the action taken if the file already exists. 




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>



<a href="https://msdn.microsoft.com/3a7744a6-feb3-4aea-856d-8496aecc0176">IDataCollector::FileNameFormat</a>



<a href="https://msdn.microsoft.com/94e6bb13-fb99-4968-8a7f-fbda1f6ea42e">IDataCollector::FileNameFormatPattern</a>
 

 

