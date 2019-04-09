---
UID: NF:sbtsv.ITsSbPluginNotifySink.OnInitialized
title: ITsSbPluginNotifySink::OnInitialized (sbtsv.h)
author: windows-sdk-content
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the plug-in has completed a call of Initialize.
old-location: termserv\itssbpluginnotifysink_oninitialized.htm
tech.root: TermServ
ms.assetid: 2fe468c9-457f-4a56-aaf9-4eb48fec8720
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbPluginNotifySink interface [Remote Desktop Services],OnInitialized method, ITsSbPluginNotifySink.OnInitialized, ITsSbPluginNotifySink::OnInitialized, OnInitialized, OnInitialized method [Remote Desktop Services], OnInitialized method [Remote Desktop Services],ITsSbPluginNotifySink interface, sbtsv/ITsSbPluginNotifySink::OnInitialized, termserv.itssbpluginnotifysink_oninitialized
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
 - ITsSbPluginNotifySink.OnInitialized
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbPluginNotifySink::OnInitialized


## -description


Notifies Remote Desktop Connection Broker (RD Connection Broker) that the plug-in has completed a call of <a href="https://msdn.microsoft.com/1ff0b1a2-042d-4df2-9ae4-cfa4b7c644ab">Initialize</a>.


## -parameters




### -param hr [in]

Specifies the result of the call to <a href="https://msdn.microsoft.com/1ff0b1a2-042d-4df2-9ae4-cfa4b7c644ab">Initialize</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Plug-ins should call this method after they complete their initialization process.




## -see-also




<a href="https://msdn.microsoft.com/c52a3253-74cb-4ff9-a4f3-cb9601c02e7d">ITsSbPluginNotifySink</a>
 

 

