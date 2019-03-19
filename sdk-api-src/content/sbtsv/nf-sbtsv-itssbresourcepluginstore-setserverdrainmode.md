---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetServerDrainMode
title: ITsSbResourcePluginStore::SetServerDrainMode (sbtsv.h)
author: windows-sdk-content
description: Sets the drain mode of the specified server.
old-location: termserv\itssbresourcepluginstore_setserverdrainmode.htm
tech.root: TermServ
ms.assetid: E0213889-7CC9-446A-9EFF-7C8B02E4A35D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetServerDrainMode method, ITsSbResourcePluginStore.SetServerDrainMode, ITsSbResourcePluginStore::SetServerDrainMode, SetServerDrainMode, SetServerDrainMode method [Remote Desktop Services], SetServerDrainMode method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::SetServerDrainMode, termserv.itssbresourcepluginstore_setserverdrainmode
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
 - ITsSbResourcePluginStore.SetServerDrainMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbResourcePluginStore::SetServerDrainMode


## -description


Sets the drain mode of the specified server.


## -parameters




### -param ServerFQDN [in]

The fully qualified domain name of the server.


### -param DrainMode [in]

The mode to set.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>
 

 

