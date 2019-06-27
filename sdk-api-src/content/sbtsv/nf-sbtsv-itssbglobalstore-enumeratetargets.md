---
UID: NF:sbtsv.ITsSbGlobalStore.EnumerateTargets
title: ITsSbGlobalStore::EnumerateTargets (sbtsv.h)
author: windows-sdk-content
description: Returns an array that contains the specified targets present in the global store.
old-location: termserv\itssbglobalstore_enumeratetargets.htm
tech.root: TermServ
ms.assetid: 939d967f-6846-4ef2-9943-a171eac6cb21
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumerateTargets, EnumerateTargets method [Remote Desktop Services], EnumerateTargets method [Remote Desktop Services],ITsSbGlobalStore interface, ITsSbGlobalStore interface [Remote Desktop Services],EnumerateTargets method, ITsSbGlobalStore.EnumerateTargets, ITsSbGlobalStore::EnumerateTargets, sbtsv/ITsSbGlobalStore::EnumerateTargets, termserv.itssbglobalstore_enumeratetargets
ms.topic: method
f1_keywords: 
 - "sbtsv/ITsSbGlobalStore.EnumerateTargets"
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbGlobalStore.EnumerateTargets
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbGlobalStore::EnumerateTargets


## -description


Returns an array that contains the specified targets present in the global store. 


## -parameters




### -param ProviderName [in]

The provider name.


### -param FarmName [in]

The farm name.


### -param EnvName [in]

The environment name.


### -param pdwCount [in, out]

The number of targets retrieved.


### -param pVal [out]

Pointer to the retrieved <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>objects.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore">ITsSbGlobalStore</a>
 

 

