---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetServerWaitingToStart
title: ITsSbResourcePluginStore::SetServerWaitingToStart
author: windows-driver-content
description: Indicates to the session host that the server is waiting to start.
old-location: termserv\itssbresourcepluginstore_setserverwaitingtostart.htm
old-project: TermServ
ms.assetid: cf677be1-387b-4a63-902b-bacda8729b23
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetServerWaitingToStart method, ITsSbResourcePluginStore.SetServerWaitingToStart, ITsSbResourcePluginStore::SetServerWaitingToStart, SetServerWaitingToStart, SetServerWaitingToStart method [Remote Desktop Services], SetServerWaitingToStart method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::SetServerWaitingToStart, termserv.itssbresourcepluginstore_setserverwaitingtostart
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
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbResourcePluginStore.SetServerWaitingToStart
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITsSbResourcePluginStore::SetServerWaitingToStart


## -description


Indicates to the session host that the server is waiting to start.


## -parameters




### -param PoolName [in]

Name of the pool.


### -param serverName [in]

Name of the server.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>
 

 

