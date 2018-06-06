---
UID: NF:sbtsv.ITsSbTaskPlugin.SetTaskQueue
title: ITsSbTaskPlugin::SetTaskQueue
author: windows-sdk-content
description: Updates a task in the queue of a Remote Desktop Connection Broker plugin.
old-location: termserv\itssbtaskplugin_settaskqueue.htm
old-project: TermServ
ms.assetid: a17e4767-5311-4f9b-9d05-cd9e35f7c5e2
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ITsSbTaskPlugin interface [Remote Desktop Services],SetTaskQueue method, ITsSbTaskPlugin.SetTaskQueue, ITsSbTaskPlugin::SetTaskQueue, SetTaskQueue, SetTaskQueue method [Remote Desktop Services], SetTaskQueue method [Remote Desktop Services],ITsSbTaskPlugin interface, sbtsv/ITsSbTaskPlugin::SetTaskQueue, termserv.itssbtaskplugin_settaskqueue
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
 - ITsSbTaskPlugin.SetTaskQueue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITsSbTaskPlugin::SetTaskQueue


## -description


Updates a task in the queue of  a Remote Desktop Connection Broker plugin.


## -parameters




### -param pszHostName [in]


### -param SbTaskInfoSize [in]


### -param pITsSbTaskInfo [in]

An array of pointers to <a href="https://msdn.microsoft.com/d24c1a64-e006-4229-a675-54f29b8ac1c2">ITsSbTaskInfo</a> objects.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/56463b47-c2f2-43b7-884f-d6fab9bebbf0">ITsSbTaskPlugin</a>
 

 

