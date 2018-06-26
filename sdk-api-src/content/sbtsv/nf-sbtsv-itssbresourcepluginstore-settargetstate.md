---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetTargetState
title: ITsSbResourcePluginStore::SetTargetState
author: windows-sdk-content
description: Sets the state of a target object.
old-location: termserv\itssbresourcepluginstore_settargetstate.htm
old-project: TermServ
ms.assetid: 5ba5c4c6-b644-45f7-8942-ee8ea543138d
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetTargetState method, ITsSbResourcePluginStore.SetTargetState, ITsSbResourcePluginStore::SetTargetState, SetTargetState, SetTargetState method [Remote Desktop Services], SetTargetState method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::SetTargetState, termserv.itssbresourcepluginstore_settargetstate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.SetTargetState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITsSbResourcePluginStore::SetTargetState


## -description


Sets the state of a target object.


## -parameters




### -param targetName [in]

The name of the target.


### -param newState [in]

The <a href="https://msdn.microsoft.com/52ef4bb9-d025-4b54-ac5b-16fa28047cc6">TARGET_STATE</a> value to set.


### -param pOldState [out]

The previous state of the target.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a>
 

 

