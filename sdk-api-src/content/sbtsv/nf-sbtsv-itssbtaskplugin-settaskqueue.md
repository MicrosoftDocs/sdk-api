---
UID: NF:sbtsv.ITsSbTaskPlugin.SetTaskQueue
title: ITsSbTaskPlugin::SetTaskQueue (sbtsv.h)
description: Updates a task in the queue of a Remote Desktop Connection Broker plugin.
helpviewer_keywords: ["ITsSbTaskPlugin interface [Remote Desktop Services]","SetTaskQueue method","ITsSbTaskPlugin.SetTaskQueue","ITsSbTaskPlugin::SetTaskQueue","SetTaskQueue","SetTaskQueue method [Remote Desktop Services]","SetTaskQueue method [Remote Desktop Services]","ITsSbTaskPlugin interface","sbtsv/ITsSbTaskPlugin::SetTaskQueue","termserv.itssbtaskplugin_settaskqueue"]
old-location: termserv\itssbtaskplugin_settaskqueue.htm
tech.root: TermServ
ms.assetid: a17e4767-5311-4f9b-9d05-cd9e35f7c5e2
ms.date: 12/05/2018
ms.keywords: ITsSbTaskPlugin interface [Remote Desktop Services],SetTaskQueue method, ITsSbTaskPlugin.SetTaskQueue, ITsSbTaskPlugin::SetTaskQueue, SetTaskQueue, SetTaskQueue method [Remote Desktop Services], SetTaskQueue method [Remote Desktop Services],ITsSbTaskPlugin interface, sbtsv/ITsSbTaskPlugin::SetTaskQueue, termserv.itssbtaskplugin_settaskqueue
f1_keywords:
- sbtsv/ITsSbTaskPlugin.SetTaskQueue
dev_langs:
- c++
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
- ITsSbTaskPlugin.SetTaskQueue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbTaskPlugin::SetTaskQueue


## -description


Updates a task in the queue of  a Remote Desktop Connection Broker plugin.


## -parameters




### -param pszHostName [in]


### -param SbTaskInfoSize [in]


### -param pITsSbTaskInfo [in]

An array of pointers to <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo">ITsSbTaskInfo</a> objects.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin">ITsSbTaskPlugin</a>
 

 

