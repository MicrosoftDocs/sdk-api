---
UID: NF:pla.IDataCollectorSet.get_SubdirectoryFormat
title: IDataCollectorSet::get_SubdirectoryFormat (pla.h)
description: Retrieves or sets flags that describe how to decorate the subdirectory name. (Get)
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","SubdirectoryFormat property","IDataCollectorSet.SubdirectoryFormat","IDataCollectorSet.get_SubdirectoryFormat","IDataCollectorSet::SubdirectoryFormat","IDataCollectorSet::get_SubdirectoryFormat","IDataCollectorSet::put_SubdirectoryFormat","SubdirectoryFormat property [PLA]","SubdirectoryFormat property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_subdirectoryformat","get_SubdirectoryFormat","pla.idatacollectorset_get_subdirectoryformat","pla/IDataCollectorSet::SubdirectoryFormat","pla/IDataCollectorSet::get_SubdirectoryFormat","pla/IDataCollectorSet::put_SubdirectoryFormat"]
old-location: pla\idatacollectorset_get_subdirectoryformat.htm
tech.root: PLA
ms.assetid: f9e6eb88-ac38-4b99-ab64-a408f75f7969
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],SubdirectoryFormat property, IDataCollectorSet.SubdirectoryFormat, IDataCollectorSet.get_SubdirectoryFormat, IDataCollectorSet::SubdirectoryFormat, IDataCollectorSet::get_SubdirectoryFormat, IDataCollectorSet::put_SubdirectoryFormat, SubdirectoryFormat property [PLA], SubdirectoryFormat property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_subdirectoryformat, get_SubdirectoryFormat, pla.idatacollectorset_get_subdirectoryformat, pla/IDataCollectorSet::SubdirectoryFormat, pla/IDataCollectorSet::get_SubdirectoryFormat, pla/IDataCollectorSet::put_SubdirectoryFormat
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
 - IDataCollectorSet::get_SubdirectoryFormat
 - pla/IDataCollectorSet::get_SubdirectoryFormat
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
 - IDataCollectorSet.SubdirectoryFormat
 - IDataCollectorSet.get_SubdirectoryFormat
 - IDataCollectorSet.put_SubdirectoryFormat
---

# IDataCollectorSet::get_SubdirectoryFormat


## -description

Retrieves or sets flags that describe how to decorate the subdirectory name.

This property is read/write.

## -parameters

## -remarks

PLA appends the decoration to the folder name. For example, if you specify <b>plaMonthDayHour</b>, PLA appends the current month, day, and hour values to the folder name. If the folder name is MyFile, the result could be MyFile110816.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectory">IDataCollectorSet::Subdirectory</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectoryformatpattern">IDataCollectorSet::SubdirectoryFormatPattern</a>
