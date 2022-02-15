---
UID: NE:comsvcs.tagCSC_SynchronizationConfig
title: CSC_SynchronizationConfig (comsvcs.h)
description: Indicates how synchronization is configured for CServiceConfig.
helpviewer_keywords: ["CSC_IfContainerIsSynchronized","CSC_NewSynchronization","CSC_NewSynchronizationIfNecessary","CSC_NoSynchronization","CSC_SynchronizationConfig","CSC_SynchronizationConfig enumeration [COM+]","_cos_CSC_SynchronizationConfig","comsvcs/CSC_IfContainerIsSynchronized","comsvcs/CSC_NewSynchronization","comsvcs/CSC_NewSynchronizationIfNecessary","comsvcs/CSC_NoSynchronization","comsvcs/CSC_SynchronizationConfig","cos.csc_synchronizationconfig"]
old-location: cos\csc_synchronizationconfig.htm
tech.root: cos
ms.assetid: dc0c4310-e2d8-462c-af55-f1513934b8ef
ms.date: 12/05/2018
ms.keywords: CSC_IfContainerIsSynchronized, CSC_NewSynchronization, CSC_NewSynchronizationIfNecessary, CSC_NoSynchronization, CSC_SynchronizationConfig, CSC_SynchronizationConfig enumeration [COM+], _cos_CSC_SynchronizationConfig, comsvcs/CSC_IfContainerIsSynchronized, comsvcs/CSC_NewSynchronization, comsvcs/CSC_NewSynchronizationIfNecessary, comsvcs/CSC_NoSynchronization, comsvcs/CSC_SynchronizationConfig, cos.csc_synchronizationconfig
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: CSC_SynchronizationConfig
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCSC_SynchronizationConfig
 - comsvcs/tagCSC_SynchronizationConfig
 - CSC_SynchronizationConfig
 - comsvcs/CSC_SynchronizationConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_SynchronizationConfig
---

# CSC_SynchronizationConfig enumeration


## -description

Indicates how synchronization is configured for <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>.

## -enum-fields

### -field CSC_NoSynchronization:0

The code is forced to run unsynchronized. This is the default synchronization setting for <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Ignore.

### -field CSC_IfContainerIsSynchronized

The code runs in the containing synchronization domain if one exists. This is the default synchronization setting for <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Inherit.

### -field CSC_NewSynchronizationIfNecessary

Synchronization is always used. The existing synchronization domain is used, or if the enclosed context does not already use synchronization, a new synchronization domain is created.

### -field CSC_NewSynchronization

A new synchronization domain is always created.

## -remarks

This enumeration is used to configure synchronization through <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> for either the work submitted through the activity created by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or the work that is enclosed between calls to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>.

Synchronization can affect the components created by the contained code even if it has no immediate impact on the contained code itself. For example, if the same code is running on two different threads and this code calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> asking for synchronization services, each thread is contained in its own synchronization domain.

If it is incompatible with the transaction setting from <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_transactionconfig">CSC_TransactionConfig</a>, the synchronization setting is increased to the minimum that is required for the transaction.

## -see-also

<a href="/windows/desktop/cossdk/com--synchronization">COM+ Synchronization</a>



<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicesynchronizationconfig-configuresynchronization">IServiceSynchronizationConfig::ConfigureSynchronization</a>
