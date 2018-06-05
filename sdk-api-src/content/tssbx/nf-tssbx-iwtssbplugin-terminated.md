---
UID: NF:tssbx.IWTSSBPlugin.Terminated
title: IWTSSBPlugin::Terminated
author: windows-sdk-content
description: Notifies the plug-in that it is about to be destroyed by Terminal Services Session Broker (TS&#160;Session Broker).
old-location: termserv\iwtssbplugin_terminated.htm
old-project: TermServ
ms.assetid: 123455dd-6ef3-409f-b021-e641868b16f0
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWTSSBPlugin interface [Remote Desktop Services],Terminated method, IWTSSBPlugin.Terminated, IWTSSBPlugin::Terminated, Terminated, Terminated method [Remote Desktop Services], Terminated method [Remote Desktop Services],IWTSSBPlugin interface, termserv.iwtssbplugin_terminated, tssbx/IWTSSBPlugin::Terminated
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTSSBX_NOTIFICATION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tssbx.h
api_name:
-	IWTSSBPlugin.Terminated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWTSSBPlugin::Terminated


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a> interface.]

 Notifies the plug-in that it is about to be destroyed by Terminal Services Session Broker (TS Session Broker).


## -parameters






## -returns



Returns <b>S_OK</b> if successful.




## -remarks



TS Session Broker calls this method before it destroys this instance of the plug-in. You can use this method to perform cleanup for the plug-in before TS Session Broker destroys it. After the plug-in is destroyed, TS Session Broker reverts to its native redirection service.

Your implementation of this method must return <b>S_OK</b> immediately if successful.




## -see-also




<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

