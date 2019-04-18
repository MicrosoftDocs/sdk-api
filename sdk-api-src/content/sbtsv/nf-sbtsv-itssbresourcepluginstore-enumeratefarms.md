---
UID: NF:sbtsv.ITsSbResourcePluginStore.EnumerateFarms
title: ITsSbResourcePluginStore::EnumerateFarms (sbtsv.h)
author: windows-sdk-content
description: Enumerates all the farms that have been added to the resource plug-in store.
old-location: termserv\itssbresourcepluginstore_enumeratefarms.htm
tech.root: TermServ
ms.assetid: 54ed82b2-531c-468b-a4d3-ad299ae1f2d8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumerateFarms, EnumerateFarms method [Remote Desktop Services], EnumerateFarms method [Remote Desktop Services],ITsSbResourcePluginStore interface, EnumerateFarms method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],EnumerateFarms method, ITsSbResourcePluginStore.EnumerateFarms, ITsSbResourcePluginStore::EnumerateFarms, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],EnumerateFarms method, ITsSbResourcePluginStoreEx::EnumerateFarms, sbtsv/ITsSbResourcePluginStore::EnumerateFarms, sbtsv/ITsSbResourcePluginStoreEx::EnumerateFarms, termserv.itssbresourcepluginstore_enumeratefarms
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
 - ITsSbResourcePluginStore.EnumerateFarms
 - ITsSbResourcePluginStoreEx.EnumerateFarms
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbResourcePluginStore::EnumerateFarms


## -description


Enumerates all the farms that have been added to the resource plug-in store.


## -parameters




### -param pdwCount [out]

The number of farms retrieved.


### -param pVal [out]

An array of farm names. The <i>pdwCount</i> parameter contains the number of elements in this array. When you have finished using the array, free the allocated memory by calling the   <a href="https://msdn.microsoft.com/fc94f7e7-b903-4c78-905c-54df1f8d13fa">SafeArrayDestroy</a> function.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>
 

 

