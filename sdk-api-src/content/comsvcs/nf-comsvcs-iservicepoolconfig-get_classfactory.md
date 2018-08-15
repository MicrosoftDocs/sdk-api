---
UID: NF:comsvcs.IServicePoolConfig.get_ClassFactory
title: IServicePoolConfig::get_ClassFactory
author: windows-sdk-content
description: Retrieves a class factory for the pooled objects.
old-location: cos\iservicepoolconfig_get_classfactory.htm
old-project: cossdk
ms.assetid: cef9ff6b-53e2-43e1-9be6-7c0d7f89c318
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IServicePoolConfig interface [COM+],get_ClassFactory method, IServicePoolConfig.get_ClassFactory, IServicePoolConfig::get_ClassFactory, comsvcs/IServicePoolConfig::get_ClassFactory, cos.iservicepoolconfig_get_classfactory, get_ClassFactory, get_ClassFactory method [COM+], get_ClassFactory method [COM+],IServicePoolConfig interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServicePoolConfig.get_ClassFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServicePoolConfig::get_ClassFactory


## -description


Retrieves a class factory for the pooled objects.


## -parameters




### -param pFactory [out]

A pointer to the <a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a> interface pointer.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/026abfcf-56b5-4821-a9d4-37beeb3a052b">IServicePoolConfig</a>
 

 

