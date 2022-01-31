---
UID: NE:comsvcs.tagCSC_ThreadPool
title: CSC_ThreadPool (comsvcs.h)
description: Indicates the thread pool in which the work runs that is submitted through the activity returned from CoCreateActivity.
helpviewer_keywords: ["CSC_MTAThreadPool","CSC_STAThreadPool","CSC_ThreadPool","CSC_ThreadPool enumeration [COM+]","CSC_ThreadPoolInherit","CSC_ThreadPoolNone","_cos_CSC_ThreadPool","comsvcs/CSC_MTAThreadPool","comsvcs/CSC_STAThreadPool","comsvcs/CSC_ThreadPool","comsvcs/CSC_ThreadPoolInherit","comsvcs/CSC_ThreadPoolNone","cos.csc_threadpool"]
old-location: cos\csc_threadpool.htm
tech.root: cos
ms.assetid: 5acf5c6b-b015-448b-ad4c-e4361a97c31e
ms.date: 12/05/2018
ms.keywords: CSC_MTAThreadPool, CSC_STAThreadPool, CSC_ThreadPool, CSC_ThreadPool enumeration [COM+], CSC_ThreadPoolInherit, CSC_ThreadPoolNone, _cos_CSC_ThreadPool, comsvcs/CSC_MTAThreadPool, comsvcs/CSC_STAThreadPool, comsvcs/CSC_ThreadPool, comsvcs/CSC_ThreadPoolInherit, comsvcs/CSC_ThreadPoolNone, cos.csc_threadpool
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
req.typenames: CSC_ThreadPool
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCSC_ThreadPool
 - comsvcs/tagCSC_ThreadPool
 - CSC_ThreadPool
 - comsvcs/CSC_ThreadPool
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
 - CSC_ThreadPool
---

# CSC_ThreadPool enumeration


## -description

Indicates the thread pool in which the work runs that is submitted through the activity returned from <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>.

## -enum-fields

### -field CSC_ThreadPoolNone:0

No thread pool is used. If this value is used to configure a <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object that is passed to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>, an error (CO_E_THREADPOOL_CONFIG) is returned. This is the default thread pool setting for <b>CServiceConfig</b> when <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Ignore.

### -field CSC_ThreadPoolInherit

The same type of thread pool apartment as the caller's thread apartment is used. If the caller's thread apartment is the neutral apartment, a single-threaded apartment is used. This is the default thread pool setting for <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Inherit.

### -field CSC_STAThreadPool

A single-threaded apartment (STA) is used.

### -field CSC_MTAThreadPool

A multithreaded apartment (MTA) is used.

## -remarks

This enumeration is used to set the thread pool for <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> only when calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>. An error is returned if you try to set the thread pool when calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>.

## -see-also

<a href="/windows/desktop/cossdk/com--threading-models">COM+ Threading Models</a>



<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicethreadpoolconfig-selectthreadpool">IServiceThreadPoolConfig::SelectThreadPool</a>
