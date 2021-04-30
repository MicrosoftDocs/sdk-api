---
UID: NF:pla.IDataCollectorSet.get_Server
title: IDataCollectorSet::get_Server (pla.h)
description: Retrieves the name of the server where the data collector set is run.
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","Server property","IDataCollectorSet.Server","IDataCollectorSet.get_Server","IDataCollectorSet::Server","IDataCollectorSet::get_Server","Server property [PLA]","Server property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_server","get_Server","pla.idatacollectorset_get_server","pla/IDataCollectorSet::Server","pla/IDataCollectorSet::get_Server"]
old-location: pla\idatacollectorset_get_server.htm
tech.root: PLA
ms.assetid: 43098848-1b1f-4ce1-a34c-62bb493aaf0e
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],Server property, IDataCollectorSet.Server, IDataCollectorSet.get_Server, IDataCollectorSet::Server, IDataCollectorSet::get_Server, Server property [PLA], Server property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_server, get_Server, pla.idatacollectorset_get_server, pla/IDataCollectorSet::Server, pla/IDataCollectorSet::get_Server
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
 - IDataCollectorSet::get_Server
 - pla/IDataCollectorSet::get_Server
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
 - IDataCollectorSet.Server
 - IDataCollectorSet.get_Server
---

# IDataCollectorSet::get_Server


## -description

Retrieves the name of the server where the data collector set is run.

This property is read-only.

## -parameters

## -remarks

The name is set when you call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">IDataCollectorSet::Commit</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>