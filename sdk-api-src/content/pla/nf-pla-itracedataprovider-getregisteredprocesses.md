---
UID: NF:pla.ITraceDataProvider.GetRegisteredProcesses
title: ITraceDataProvider::GetRegisteredProcesses (pla.h)
description: Retrieves a list of processes that have registered as an Event Tracing for Windows (ETW) provider.
helpviewer_keywords: ["GetRegisteredProcesses","GetRegisteredProcesses method [PLA]","GetRegisteredProcesses method [PLA]","ITraceDataProvider interface","ITraceDataProvider interface [PLA]","GetRegisteredProcesses method","ITraceDataProvider.GetRegisteredProcesses","ITraceDataProvider::GetRegisteredProcesses","pla.itracedataprovider_getregisteredprocesses","pla/ITraceDataProvider::GetRegisteredProcesses"]
old-location: pla\itracedataprovider_getregisteredprocesses.htm
tech.root: PLA
ms.assetid: f848f209-c761-41aa-8e9f-4b7e2ecb54ae
ms.date: 12/05/2018
ms.keywords: GetRegisteredProcesses, GetRegisteredProcesses method [PLA], GetRegisteredProcesses method [PLA],ITraceDataProvider interface, ITraceDataProvider interface [PLA],GetRegisteredProcesses method, ITraceDataProvider.GetRegisteredProcesses, ITraceDataProvider::GetRegisteredProcesses, pla.itracedataprovider_getregisteredprocesses, pla/ITraceDataProvider::GetRegisteredProcesses
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
 - ITraceDataProvider::GetRegisteredProcesses
 - pla/ITraceDataProvider::GetRegisteredProcesses
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
 - ITraceDataProvider.GetRegisteredProcesses
---

# ITraceDataProvider::GetRegisteredProcesses


## -description

Retrieves a list of processes that have registered as an Event Tracing for Windows (ETW) provider.

## -parameters

### -param Processes [out]

An <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a> interface that contains the list of processes that have registered as an ETW provider. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_key">IValueMapItem::Key</a> property  contains the name of the binary, and the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_value">IValueMapItem::Value</a> property contains the process identifier.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">ITraceDataProvider</a>