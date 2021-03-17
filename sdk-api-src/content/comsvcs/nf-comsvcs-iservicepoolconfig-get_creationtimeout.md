---
UID: NF:comsvcs.IServicePoolConfig.get_CreationTimeout
title: IServicePoolConfig::get_CreationTimeout (comsvcs.h)
description: Retrieves the time-out interval for activating a pooled object.
helpviewer_keywords: ["IServicePoolConfig interface [COM+]","get_CreationTimeout method","IServicePoolConfig.get_CreationTimeout","IServicePoolConfig::get_CreationTimeout","comsvcs/IServicePoolConfig::get_CreationTimeout","cos.iservicepoolconfig_get_creationtimeout","get_CreationTimeout","get_CreationTimeout method [COM+]","get_CreationTimeout method [COM+]","IServicePoolConfig interface"]
old-location: cos\iservicepoolconfig_get_creationtimeout.htm
tech.root: cos
ms.assetid: fcedf01c-2780-40dc-9ac9-70e267592fa0
ms.date: 12/05/2018
ms.keywords: IServicePoolConfig interface [COM+],get_CreationTimeout method, IServicePoolConfig.get_CreationTimeout, IServicePoolConfig::get_CreationTimeout, comsvcs/IServicePoolConfig::get_CreationTimeout, cos.iservicepoolconfig_get_creationtimeout, get_CreationTimeout, get_CreationTimeout method [COM+], get_CreationTimeout method [COM+],IServicePoolConfig interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IServicePoolConfig::get_CreationTimeout
 - comsvcs/IServicePoolConfig::get_CreationTimeout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServicePoolConfig.get_CreationTimeout
---

# IServicePoolConfig::get_CreationTimeout


## -description

Retrieves the time-out interval for activating a pooled object.

## -parameters

### -param pdwCreationTimeout [out]

The time-out interval.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a>