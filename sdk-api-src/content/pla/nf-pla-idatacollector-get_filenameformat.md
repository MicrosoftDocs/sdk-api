---
UID: NF:pla.IDataCollector.get_FileNameFormat
title: IDataCollector::get_FileNameFormat (pla.h)
description: Retrieves or sets flags that describe how to decorate the file name.helpviewer_keywords: ["FileNameFormat property [PLA]","FileNameFormat property [PLA]","IDataCollector interface","IDataCollector interface [PLA]","FileNameFormat property","IDataCollector.FileNameFormat","IDataCollector.get_FileNameFormat","IDataCollector::FileNameFormat","IDataCollector::get_FileNameFormat","IDataCollector::put_FileNameFormat","base.idatacollector_filenameformat","get_FileNameFormat","pla.idatacollector_filenameformat","pla/IDataCollector::FileNameFormat","pla/IDataCollector::get_FileNameFormat","pla/IDataCollector::put_FileNameFormat"]
old-location: pla\idatacollector_filenameformat.htm
tech.root: PLA
ms.assetid: 3a7744a6-feb3-4aea-856d-8496aecc0176
ms.date: 12/05/2018
ms.keywords: FileNameFormat property [PLA], FileNameFormat property [PLA],IDataCollector interface, IDataCollector interface [PLA],FileNameFormat property, IDataCollector.FileNameFormat, IDataCollector.get_FileNameFormat, IDataCollector::FileNameFormat, IDataCollector::get_FileNameFormat, IDataCollector::put_FileNameFormat, base.idatacollector_filenameformat, get_FileNameFormat, pla.idatacollector_filenameformat, pla/IDataCollector::FileNameFormat, pla/IDataCollector::get_FileNameFormat, pla/IDataCollector::put_FileNameFormat
f1_keywords:
- pla/IDataCollector.FileNameFormat
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Pla.dll
api_name:
- IDataCollector.FileNameFormat
- IDataCollector.get_FileNameFormat
- IDataCollector.put_FileNameFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataCollector::get_FileNameFormat


## -description


Retrieves or sets flags that describe how to decorate the file name.

This property is read/write.


## -parameters


## -remarks



PLA appends the decoration to the file name. For example, if you specify <b>plaMonthDayHour</b>, PLA appends the current month, day, and hour values to the file name. If the file name is MyFile, the result could be MyFile110816.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filename">IDataCollector::FileName</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformatpattern">IDataCollector::FileNameFormatPattern</a>
 

 

