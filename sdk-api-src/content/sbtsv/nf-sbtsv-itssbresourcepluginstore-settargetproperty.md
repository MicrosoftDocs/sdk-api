---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetTargetProperty
title: ITsSbResourcePluginStore::SetTargetProperty
author: windows-sdk-content
description: Sets the value of a property of a target.
old-location: termserv\itssbresourcepluginstore_settargetproperty.htm
old-project: TermServ
ms.assetid: 11d03b69-a7d0-4930-ba9c-a9373706580c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetTargetProperty method, ITsSbResourcePluginStore.SetTargetProperty, ITsSbResourcePluginStore::SetTargetProperty, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],SetTargetProperty method, ITsSbResourcePluginStoreEx::SetTargetProperty, SetTargetProperty, SetTargetProperty method [Remote Desktop Services], SetTargetProperty method [Remote Desktop Services],ITsSbResourcePluginStore interface, SetTargetProperty method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::SetTargetProperty, sbtsv/ITsSbResourcePluginStoreEx::SetTargetProperty, termserv.itssbresourcepluginstore_settargetproperty
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
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbResourcePluginStore.SetTargetProperty
-	ITsSbResourcePluginStoreEx.SetTargetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITsSbResourcePluginStore::SetTargetProperty


## -description


Sets the value of a  property of a target.


## -parameters




### -param TargetName [in]

The name of the target.


### -param PropertyName [in]

The name of the property.


### -param pProperty [in]

A pointer to the value to set.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>



<a href="https://msdn.microsoft.com/51b5e267-da1a-4d83-81bc-0cf8fb525fa9">SetTargetPropertyWithVersionCheck</a>
 

 

