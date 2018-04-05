---
UID: NF:sbtsv.ITsSbTaskPlugin.InitializeTaskPlugin
title: ITsSbTaskPlugin::InitializeTaskPlugin method
author: windows-driver-content
description: Initializes a task that is in the queue of a Remote Desktop Connection Broker plugin.
old-location: termserv\itssbtaskplugin_initializetaskplugin.htm
old-project: TermServ
ms.assetid: 9e8722c4-0070-448a-a97c-aeb1db59ac7b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ITsSbTaskPlugin, ITsSbTaskPlugin interface [Remote Desktop Services], InitializeTaskPlugin method, ITsSbTaskPlugin::InitializeTaskPlugin, InitializeTaskPlugin method [Remote Desktop Services], InitializeTaskPlugin method [Remote Desktop Services], ITsSbTaskPlugin interface, InitializeTaskPlugin,ITsSbTaskPlugin.InitializeTaskPlugin, sbtsv/ITsSbTaskPlugin::InitializeTaskPlugin, termserv.itssbtaskplugin_initializetaskplugin
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
-	ITsSbTaskPlugin.InitializeTaskPlugin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITsSbTaskPlugin::InitializeTaskPlugin method


## -description


Initializes a task that is in the queue of a Remote Desktop Connection Broker plugin.


## -parameters




### -param pITsSbTaskPluginNotifySink [in]

A pointer to an <a href="https://msdn.microsoft.com/dc1b56f3-ea5f-4df5-b90a-ce24c36aee21">ITsSbTaskPluginNotifySink</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/56463b47-c2f2-43b7-884f-d6fab9bebbf0">ITsSbTaskPlugin</a>
 

 

