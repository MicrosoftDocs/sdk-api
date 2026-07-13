---
UID: NF:sbtsv.ITsSbPluginNotifySink.OnInitialized
title: ITsSbPluginNotifySink::OnInitialized (sbtsv.h)
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the plug-in has completed a call of Initialize.
helpviewer_keywords: ["ITsSbPluginNotifySink interface [Remote Desktop Services]","OnInitialized method","ITsSbPluginNotifySink.OnInitialized","ITsSbPluginNotifySink::OnInitialized","OnInitialized","OnInitialized method [Remote Desktop Services]","OnInitialized method [Remote Desktop Services]","ITsSbPluginNotifySink interface","sbtsv/ITsSbPluginNotifySink::OnInitialized","termserv.itssbpluginnotifysink_oninitialized"]
old-location: termserv\itssbpluginnotifysink_oninitialized.htm
tech.root: TermServ
ms.assetid: 2fe468c9-457f-4a56-aaf9-4eb48fec8720
ms.date: 12/05/2018
ms.keywords: ITsSbPluginNotifySink interface [Remote Desktop Services],OnInitialized method, ITsSbPluginNotifySink.OnInitialized, ITsSbPluginNotifySink::OnInitialized, OnInitialized, OnInitialized method [Remote Desktop Services], OnInitialized method [Remote Desktop Services],ITsSbPluginNotifySink interface, sbtsv/ITsSbPluginNotifySink::OnInitialized, termserv.itssbpluginnotifysink_oninitialized
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
 - ITsSbPluginNotifySink::OnInitialized
 - sbtsv/ITsSbPluginNotifySink::OnInitialized
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
 - ITsSbPluginNotifySink.OnInitialized
---

# ITsSbPluginNotifySink::OnInitialized


## -description

Notifies Remote Desktop Connection Broker (RD Connection Broker) that the plug-in has completed a call of <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbplugin-initialize">Initialize</a>.

## -parameters

### -param hr [in]

Specifies the result of the call to <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbplugin-initialize">Initialize</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Plug-ins should call this method after they complete their initialization process.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink">ITsSbPluginNotifySink</a>