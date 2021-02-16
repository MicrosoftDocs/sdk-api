---
UID: NF:pla.IDataCollectorSet.get_Name
title: IDataCollectorSet::get_Name (pla.h)
description: Retrieves the unique name used to identify the data collector set.
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","Name property","IDataCollectorSet.Name","IDataCollectorSet.get_Name","IDataCollectorSet::Name","IDataCollectorSet::get_Name","Name property [PLA]","Name property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_name","get_Name","pla.idatacollectorset_get_name","pla/IDataCollectorSet::Name","pla/IDataCollectorSet::get_Name"]
old-location: pla\idatacollectorset_get_name.htm
tech.root: PLA
ms.assetid: 69f6af39-b614-4957-a1e5-1f381c915f17
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],Name property, IDataCollectorSet.Name, IDataCollectorSet.get_Name, IDataCollectorSet::Name, IDataCollectorSet::get_Name, Name property [PLA], Name property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_name, get_Name, pla.idatacollectorset_get_name, pla/IDataCollectorSet::Name, pla/IDataCollectorSet::get_Name
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
 - IDataCollectorSet::get_Name
 - pla/IDataCollectorSet::get_Name
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
 - IDataCollectorSet.Name
 - IDataCollectorSet.get_Name
---

# IDataCollectorSet::get_Name


## -description

Retrieves the unique name used to identify the data collector set.

This property is read-only.

## -parameters

## -remarks

The name is set when you call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">IDataCollectorSet::Commit</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>