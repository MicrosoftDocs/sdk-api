---
UID: NF:pla.IDataCollector.put_FileNameFormat
title: IDataCollector::put_FileNameFormat
author: windows-sdk-content
description: Retrieves or sets flags that describe how to decorate the file name.
old-location: pla\idatacollector_filenameformat.htm
tech.root: PLA
ms.assetid: 3a7744a6-feb3-4aea-856d-8496aecc0176
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: FileNameFormat property [PLA], FileNameFormat property [PLA],IDataCollector interface, IDataCollector interface [PLA],FileNameFormat property, IDataCollector.FileNameFormat, IDataCollector.put_FileNameFormat, IDataCollector::FileNameFormat, IDataCollector::get_FileNameFormat, IDataCollector::put_FileNameFormat, base.idatacollector_filenameformat, pla.idatacollector_filenameformat, pla/IDataCollector::FileNameFormat, pla/IDataCollector::get_FileNameFormat, pla/IDataCollector::put_FileNameFormat, put_FileNameFormat
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollector::put_FileNameFormat


## -description


Retrieves or sets flags that describe how to decorate the file name.

This property is read/write.


## -parameters


## -remarks



PLA appends the decoration to the file name. For example, if you specify <b>plaMonthDayHour</b>, PLA appends the current month, day, and hour values to the file name. If the file name is MyFile, the result could be MyFile110816.




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>



<a href="https://msdn.microsoft.com/9208baf8-0bc7-45c4-a912-7b59f4c1ca6a">IDataCollector::FileName</a>



<a href="https://msdn.microsoft.com/94e6bb13-fb99-4968-8a7f-fbda1f6ea42e">IDataCollector::FileNameFormatPattern</a>
 

 

