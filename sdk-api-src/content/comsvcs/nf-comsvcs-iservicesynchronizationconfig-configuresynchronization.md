---
UID: NF:comsvcs.IServiceSynchronizationConfig.ConfigureSynchronization
title: IServiceSynchronizationConfig::ConfigureSynchronization (comsvcs.h)
description: Configures the synchronization for the enclosed work.
helpviewer_keywords: ["ConfigureSynchronization","ConfigureSynchronization method [COM+]","ConfigureSynchronization method [COM+]","IServiceSynchronizationConfig interface","IServiceSynchronizationConfig interface [COM+]","ConfigureSynchronization method","IServiceSynchronizationConfig.ConfigureSynchronization","IServiceSynchronizationConfig::ConfigureSynchronization","_cos_IServiceSynchronizationConfig_ConfigureSynchronization","comsvcs/IServiceSynchronizationConfig::ConfigureSynchronization","cos.iservicesynchronizationconfig_configuresynchronization"]
old-location: cos\iservicesynchronizationconfig_configuresynchronization.htm
tech.root: cos
ms.assetid: 83fe6958-6639-4468-a3f5-3322316ccbc4
ms.date: 12/05/2018
ms.keywords: ConfigureSynchronization, ConfigureSynchronization method [COM+], ConfigureSynchronization method [COM+],IServiceSynchronizationConfig interface, IServiceSynchronizationConfig interface [COM+],ConfigureSynchronization method, IServiceSynchronizationConfig.ConfigureSynchronization, IServiceSynchronizationConfig::ConfigureSynchronization, _cos_IServiceSynchronizationConfig_ConfigureSynchronization, comsvcs/IServiceSynchronizationConfig::ConfigureSynchronization, cos.iservicesynchronizationconfig_configuresynchronization
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
 - IServiceSynchronizationConfig::ConfigureSynchronization
 - comsvcs/IServiceSynchronizationConfig::ConfigureSynchronization
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
 - IServiceSynchronizationConfig.ConfigureSynchronization
---

# IServiceSynchronizationConfig::ConfigureSynchronization


## -description

Configures the synchronization for the enclosed work.

## -parameters

### -param synchConfig [in]

 A value from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_synchronizationconfig">CSC_SynchronizationConfig</a> enumeration.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicesynchronizationconfig">IServiceSynchronizationConfig</a>