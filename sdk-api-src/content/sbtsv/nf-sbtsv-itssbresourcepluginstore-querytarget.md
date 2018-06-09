---
UID: NF:sbtsv.ITsSbResourcePluginStore.QueryTarget
title: ITsSbResourcePluginStore::QueryTarget
author: windows-sdk-content
description: Returns the target that has the specified target name and farm name.
old-location: termserv\itssbresourcepluginstore_querytarget.htm
old-project: TermServ
ms.assetid: ef78c055-edf6-4f0c-b47c-836ef85310bf
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],QueryTarget method, ITsSbResourcePluginStore.QueryTarget, ITsSbResourcePluginStore::QueryTarget, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],QueryTarget method, ITsSbResourcePluginStoreEx::QueryTarget, QueryTarget, QueryTarget method [Remote Desktop Services], QueryTarget method [Remote Desktop Services],ITsSbResourcePluginStore interface, QueryTarget method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::QueryTarget, sbtsv/ITsSbResourcePluginStoreEx::QueryTarget, termserv.itssbresourcepluginstore_querytarget
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
 - ITsSbResourcePluginStore.QueryTarget
 - ITsSbResourcePluginStoreEx.QueryTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITsSbResourcePluginStore::QueryTarget


## -description


Returns the target that has the specified target name and farm name.


## -parameters




### -param TargetName [in]

The target name.


### -param FarmName [in]

The farm name. If this parameter is <b>NULL</b>, the method returns the first target it finds.


### -param ppTarget [out]

A pointer to a pointer to an  <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a> target object. When you have finished using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A resource plug-in store can use this method to retrieve the target that has the specified target name and farm name. Unlike the global store, the resource plug-in store does not copy the target object retrieved because the resource plug-in owns the target object. Accordingly, if you modify the <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a> object that is returned by this method, you are modifying the target object in    the            resource plug-in store.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>



<a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a>
 

 

