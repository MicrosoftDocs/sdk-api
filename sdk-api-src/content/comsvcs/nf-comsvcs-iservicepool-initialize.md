---
UID: NF:comsvcs.IServicePool.Initialize
title: IServicePool::Initialize (comsvcs.h)
description: Initializes an object pool.
helpviewer_keywords: ["IServicePool interface [COM+]","Initialize method","IServicePool.Initialize","IServicePool::Initialize","Initialize","Initialize method [COM+]","Initialize method [COM+]","IServicePool interface","_cos_IServicePool_Initialize","comsvcs/IServicePool::Initialize","cos.iservicepool_initialize"]
old-location: cos\iservicepool_initialize.htm
tech.root: cos
ms.assetid: 93e88990-1737-4db4-aa37-0fe19a7ca0f3
ms.date: 12/05/2018
ms.keywords: IServicePool interface [COM+],Initialize method, IServicePool.Initialize, IServicePool::Initialize, Initialize, Initialize method [COM+], Initialize method [COM+],IServicePool interface, _cos_IServicePool_Initialize, comsvcs/IServicePool::Initialize, cos.iservicepool_initialize
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional with SP4, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
 - IServicePool::Initialize
 - comsvcs/IServicePool::Initialize
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
 - IServicePool.Initialize
---

# IServicePool::Initialize


## -description

Initializes an object pool.

## -parameters

### -param pPoolConfig [in]

An object supporting the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a> interface that describes the configuration of the object pool.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_ALREADYINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicepool-initialize">Initialize</a> has already been called.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepool">IServicePool</a>