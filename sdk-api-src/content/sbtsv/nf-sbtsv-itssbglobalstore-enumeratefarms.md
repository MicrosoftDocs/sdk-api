---
UID: NF:sbtsv.ITsSbGlobalStore.EnumerateFarms
title: ITsSbGlobalStore::EnumerateFarms
author: windows-sdk-content
description: Enumerates all the farms that have been added by the specified resource plug-in.
old-location: termserv\itssbglobalstore_enumeratefarms.htm
tech.root: termserv
ms.assetid: 51c59f35-667c-4723-aa7b-e8250bbdabe9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EnumerateFarms, EnumerateFarms method [Remote Desktop Services], EnumerateFarms method [Remote Desktop Services],ITsSbGlobalStore interface, ITsSbGlobalStore interface [Remote Desktop Services],EnumerateFarms method, ITsSbGlobalStore.EnumerateFarms, ITsSbGlobalStore::EnumerateFarms, sbtsv/ITsSbGlobalStore::EnumerateFarms, termserv.itssbglobalstore_enumeratefarms
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ITsSbGlobalStore.EnumerateFarms
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbGlobalStore::EnumerateFarms


## -description


Enumerates all the farms that have been added by the specified resource 
plug-in.


## -parameters




### -param ProviderName [in]

The provider name of the resource plug-in.


### -param pdwCount [out]

The count of farms retrieved.


### -param pVal [out]

A pointer to an array of farm names. The number of elements in this array is specified by the <i>pdwCount</i> parameter. When you have finished using the array, free the allocated memory by calling the <a href="fc94f7e7-b903-4c78-905c-54df1f8d13fa">SafeArrayDestroy</a> function.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d25b6f73-ee5f-40e4-9c49-fd48dd3990d2">ITsSbGlobalStore</a>
 

 

