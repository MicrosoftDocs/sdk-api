---
UID: NF:sbtsv.ITsSbResourcePluginStore.ReleaseTargetLock
title: ITsSbResourcePluginStore::ReleaseTargetLock
author: windows-sdk-content
description: Releases a lock on a target.
old-location: termserv\itssbresourcepluginstore_releasetargetlock.htm
tech.root: termserv
ms.assetid: 37c22f94-c00d-471b-bd6c-067b3229f99b
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],ReleaseTargetLock method, ITsSbResourcePluginStore.ReleaseTargetLock, ITsSbResourcePluginStore::ReleaseTargetLock, ReleaseTargetLock, ReleaseTargetLock method [Remote Desktop Services], ReleaseTargetLock method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::ReleaseTargetLock, termserv.itssbresourcepluginstore_releasetargetlock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ITsSbResourcePluginStore.ReleaseTargetLock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbResourcePluginStore::ReleaseTargetLock


## -description


Releases a lock on a target.


## -parameters




### -param pContext [in]

A pointer to the context returned by the <a href="https://msdn.microsoft.com/ee6f22cf-c111-4a11-ab84-b52904a148b6">AcquireTargetLock</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>
 

 

