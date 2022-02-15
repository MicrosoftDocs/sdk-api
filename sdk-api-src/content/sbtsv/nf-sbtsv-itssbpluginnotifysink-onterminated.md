---
UID: NF:sbtsv.ITsSbPluginNotifySink.OnTerminated
title: ITsSbPluginNotifySink::OnTerminated (sbtsv.h)
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the plug-in has completed a call of Terminate.
helpviewer_keywords: ["ITsSbPluginNotifySink interface [Remote Desktop Services]","OnTerminated method","ITsSbPluginNotifySink.OnTerminated","ITsSbPluginNotifySink::OnTerminated","OnTerminated","OnTerminated method [Remote Desktop Services]","OnTerminated method [Remote Desktop Services]","ITsSbPluginNotifySink interface","sbtsv/ITsSbPluginNotifySink::OnTerminated","termserv.itssbpluginnotifysink_onterminated"]
old-location: termserv\itssbpluginnotifysink_onterminated.htm
tech.root: TermServ
ms.assetid: 554139f5-dd20-4bca-8eae-4621535616e6
ms.date: 12/05/2018
ms.keywords: ITsSbPluginNotifySink interface [Remote Desktop Services],OnTerminated method, ITsSbPluginNotifySink.OnTerminated, ITsSbPluginNotifySink::OnTerminated, OnTerminated, OnTerminated method [Remote Desktop Services], OnTerminated method [Remote Desktop Services],ITsSbPluginNotifySink interface, sbtsv/ITsSbPluginNotifySink::OnTerminated, termserv.itssbpluginnotifysink_onterminated
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
 - ITsSbPluginNotifySink::OnTerminated
 - sbtsv/ITsSbPluginNotifySink::OnTerminated
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
 - ITsSbPluginNotifySink.OnTerminated
---

# ITsSbPluginNotifySink::OnTerminated


## -description

Notifies Remote Desktop Connection Broker (RD Connection Broker) that the plug-in has completed a call of <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbplugin-terminate">Terminate</a>.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Plug-ins should call this method after they complete their termination process or after throwing a fatal exception.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink">ITsSbPluginNotifySink</a>
