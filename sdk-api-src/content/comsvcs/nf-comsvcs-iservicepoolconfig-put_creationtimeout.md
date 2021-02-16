---
UID: NF:comsvcs.IServicePoolConfig.put_CreationTimeout
title: IServicePoolConfig::put_CreationTimeout (comsvcs.h)
description: Sets the time-out interval for activating a pooled object.
helpviewer_keywords: ["IServicePoolConfig interface [COM+]","put_CreationTimeout method","IServicePoolConfig.put_CreationTimeout","IServicePoolConfig::put_CreationTimeout","comsvcs/IServicePoolConfig::put_CreationTimeout","cos.iservicepoolconfig_put_creationtimeout","put_CreationTimeout","put_CreationTimeout method [COM+]","put_CreationTimeout method [COM+]","IServicePoolConfig interface"]
old-location: cos\iservicepoolconfig_put_creationtimeout.htm
tech.root: cos
ms.assetid: 04beabf7-831d-4c53-880e-f1fc22f2f20d
ms.date: 12/05/2018
ms.keywords: IServicePoolConfig interface [COM+],put_CreationTimeout method, IServicePoolConfig.put_CreationTimeout, IServicePoolConfig::put_CreationTimeout, comsvcs/IServicePoolConfig::put_CreationTimeout, cos.iservicepoolconfig_put_creationtimeout, put_CreationTimeout, put_CreationTimeout method [COM+], put_CreationTimeout method [COM+],IServicePoolConfig interface
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
 - IServicePoolConfig::put_CreationTimeout
 - comsvcs/IServicePoolConfig::put_CreationTimeout
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
 - IServicePoolConfig.put_CreationTimeout
---

# IServicePoolConfig::put_CreationTimeout


## -description

Sets the time-out interval for activating a pooled object.

## -parameters

### -param dwCreationTimeout [in]

The time-out interval.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a>