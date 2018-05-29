---
UID: NF:pla.IDataCollectorSet.get_SubdirectoryFormat
title: IDataCollectorSet::get_SubdirectoryFormat
author: windows-sdk-content
description: Retrieves or sets flags that describe how to decorate the subdirectory name.
old-location: pla\idatacollectorset_get_subdirectoryformat.htm
old-project: PLA
ms.assetid: f9e6eb88-ac38-4b99-ab64-a408f75f7969
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IDataCollectorSet interface [PLA],SubdirectoryFormat property, IDataCollectorSet.SubdirectoryFormat, IDataCollectorSet.get_SubdirectoryFormat, IDataCollectorSet::SubdirectoryFormat, IDataCollectorSet::get_SubdirectoryFormat, IDataCollectorSet::put_SubdirectoryFormat, SubdirectoryFormat property [PLA], SubdirectoryFormat property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_subdirectoryformat, get_SubdirectoryFormat, pla.idatacollectorset_get_subdirectoryformat, pla/IDataCollectorSet::SubdirectoryFormat, pla/IDataCollectorSet::get_SubdirectoryFormat, pla/IDataCollectorSet::put_SubdirectoryFormat
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IDataCollectorSet.SubdirectoryFormat
-	IDataCollectorSet.get_SubdirectoryFormat
-	IDataCollectorSet.put_SubdirectoryFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IDataCollectorSet::get_SubdirectoryFormat


## -description


Retrieves or sets flags that describe how to decorate the subdirectory name.

This property is read/write.


## -parameters


## -remarks



PLA appends the decoration to the folder name. For example, if you specify <b>plaMonthDayHour</b>, PLA appends the current month, day, and hour values to the folder name. If the folder name is MyFile, the result could be MyFile110816.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/c2c55fd9-3b29-46be-9792-acb095b1c0e4">IDataCollectorSet::Subdirectory</a>



<a href="https://msdn.microsoft.com/83b7df10-8b00-4d64-bf71-2c68e037ab3f">IDataCollectorSet::SubdirectoryFormatPattern</a>
 

 

