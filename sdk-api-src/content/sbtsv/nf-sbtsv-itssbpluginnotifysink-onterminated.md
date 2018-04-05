---
UID: NF:sbtsv.ITsSbPluginNotifySink.OnTerminated
title: ITsSbPluginNotifySink::OnTerminated method
author: windows-driver-content
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the plug-in has completed a call of Terminate.
old-location: termserv\itssbpluginnotifysink_onterminated.htm
old-project: TermServ
ms.assetid: 554139f5-dd20-4bca-8eae-4621535616e6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ITsSbPluginNotifySink, ITsSbPluginNotifySink interface [Remote Desktop Services], OnTerminated method, ITsSbPluginNotifySink::OnTerminated, OnTerminated method [Remote Desktop Services], OnTerminated method [Remote Desktop Services], ITsSbPluginNotifySink interface, OnTerminated,ITsSbPluginNotifySink.OnTerminated, sbtsv/ITsSbPluginNotifySink::OnTerminated, termserv.itssbpluginnotifysink_onterminated
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
-	ITsSbPluginNotifySink.OnTerminated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITsSbPluginNotifySink::OnTerminated method


## -description


Notifies Remote Desktop Connection Broker (RD Connection Broker) that the plug-in has completed a call of <a href="https://msdn.microsoft.com/c47c6231-f967-4239-afd4-a87e9d8f49c2">Terminate</a>.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Plug-ins should call this method after they complete their termination process or after throwing a fatal exception.




## -see-also




<a href="https://msdn.microsoft.com/c52a3253-74cb-4ff9-a4f3-cb9601c02e7d">ITsSbPluginNotifySink</a>
 

 

