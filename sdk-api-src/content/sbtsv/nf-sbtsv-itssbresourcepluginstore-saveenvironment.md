---
UID: NF:sbtsv.ITsSbResourcePluginStore.SaveEnvironment
title: ITsSbResourcePluginStore::SaveEnvironment
author: windows-sdk-content
description: Saves an environment.
old-location: termserv\itssbresourcepluginstore_saveenvironment.htm
tech.root: termserv
ms.assetid: 941d5040-e6e4-4f7e-be31-2b52eb16fa9f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SaveEnvironment method, ITsSbResourcePluginStore.SaveEnvironment, ITsSbResourcePluginStore::SaveEnvironment, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],SaveEnvironment method, ITsSbResourcePluginStoreEx::SaveEnvironment, SaveEnvironment, SaveEnvironment method [Remote Desktop Services], SaveEnvironment method [Remote Desktop Services],ITsSbResourcePluginStore interface, SaveEnvironment method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::SaveEnvironment, sbtsv/ITsSbResourcePluginStoreEx::SaveEnvironment, termserv.itssbresourcepluginstore_saveenvironment
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
 - ITsSbResourcePluginStore.SaveEnvironment
 - ITsSbResourcePluginStoreEx.SaveEnvironment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- sbtsv.h
: 
- ITsSbResourcePluginStore.SaveEnvironment
: 
---

# ITsSbResourcePluginStore::SaveEnvironment


## -description


Saves an environment.


## -parameters




### -param pEnvironment [in]

Pointer to the <a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a> object to save.


### -param bForceWrite [in]

Set to <b>TRUE</b> to force writing the saved object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>
 

 

