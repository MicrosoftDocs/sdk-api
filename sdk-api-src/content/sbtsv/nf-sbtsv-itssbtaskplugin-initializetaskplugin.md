---
UID: NF:sbtsv.ITsSbTaskPlugin.InitializeTaskPlugin
title: ITsSbTaskPlugin::InitializeTaskPlugin (sbtsv.h)
description: Initializes a task that is in the queue of a Remote Desktop Connection Broker plugin.
helpviewer_keywords: ["ITsSbTaskPlugin interface [Remote Desktop Services]","InitializeTaskPlugin method","ITsSbTaskPlugin.InitializeTaskPlugin","ITsSbTaskPlugin::InitializeTaskPlugin","InitializeTaskPlugin","InitializeTaskPlugin method [Remote Desktop Services]","InitializeTaskPlugin method [Remote Desktop Services]","ITsSbTaskPlugin interface","sbtsv/ITsSbTaskPlugin::InitializeTaskPlugin","termserv.itssbtaskplugin_initializetaskplugin"]
old-location: termserv\itssbtaskplugin_initializetaskplugin.htm
tech.root: TermServ
ms.assetid: 9e8722c4-0070-448a-a97c-aeb1db59ac7b
ms.date: 12/05/2018
ms.keywords: ITsSbTaskPlugin interface [Remote Desktop Services],InitializeTaskPlugin method, ITsSbTaskPlugin.InitializeTaskPlugin, ITsSbTaskPlugin::InitializeTaskPlugin, InitializeTaskPlugin, InitializeTaskPlugin method [Remote Desktop Services], InitializeTaskPlugin method [Remote Desktop Services],ITsSbTaskPlugin interface, sbtsv/ITsSbTaskPlugin::InitializeTaskPlugin, termserv.itssbtaskplugin_initializetaskplugin
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbTaskPlugin::InitializeTaskPlugin
 - sbtsv/ITsSbTaskPlugin::InitializeTaskPlugin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbTaskPlugin.InitializeTaskPlugin
---

# ITsSbTaskPlugin::InitializeTaskPlugin


## -description

Initializes a task that is in the queue of a Remote Desktop Connection Broker plugin.

## -parameters

### -param pITsSbTaskPluginNotifySink [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink">ITsSbTaskPluginNotifySink</a> object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin">ITsSbTaskPlugin</a>