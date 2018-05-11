---
UID: NF:sbtsv.ITsSbResourcePluginStore.QueryEnvironment
title: ITsSbResourcePluginStore::QueryEnvironment
author: windows-driver-content
description: Returns the specified environment object.
old-location: termserv\itssbresourcepluginstore_queryenvironment.htm
old-project: TermServ
ms.assetid: 1497c638-ba9d-467e-8fbb-8467a43666cc
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],QueryEnvironment method, ITsSbResourcePluginStore.QueryEnvironment, ITsSbResourcePluginStore::QueryEnvironment, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],QueryEnvironment method, ITsSbResourcePluginStoreEx::QueryEnvironment, QueryEnvironment, QueryEnvironment method [Remote Desktop Services], QueryEnvironment method [Remote Desktop Services],ITsSbResourcePluginStore interface, QueryEnvironment method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, sbtsv/ITsSbResourcePluginStore::QueryEnvironment, sbtsv/ITsSbResourcePluginStoreEx::QueryEnvironment, termserv.itssbresourcepluginstore_queryenvironment
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
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbResourcePluginStore.QueryEnvironment
-	ITsSbResourcePluginStoreEx.QueryEnvironment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITsSbResourcePluginStore::QueryEnvironment


## -description


Returns the specified environment object.


## -parameters




### -param EnvironmentName [in]

The name of the environment.


### -param ppEnvironment [out]

A pointer to the retrieved <a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a> environment object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a>



<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>
 

 

