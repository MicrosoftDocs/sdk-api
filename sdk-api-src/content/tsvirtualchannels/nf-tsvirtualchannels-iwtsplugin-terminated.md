---
UID: NF:tsvirtualchannels.IWTSPlugin.Terminated
title: IWTSPlugin::Terminated
author: windows-driver-content
description: Notifies the plug-in that the Remote Desktop Connection (RDC) client has terminated.
old-location: termserv\iwtsplugin_terminated.htm
old-project: TermServ
ms.assetid: face8f79-f02d-465f-b716-1fa170fd6a33
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IWTSPlugin interface [Remote Desktop Services],Terminated method, IWTSPlugin.Terminated, IWTSPlugin::Terminated, Terminated, Terminated method [Remote Desktop Services], Terminated method [Remote Desktop Services],IWTSPlugin interface, termserv.iwtsplugin_terminated, tsvirtualchannels/IWTSPlugin::Terminated
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TsVirtualChannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTSSBX_SESSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	TsVirtualChannels.h
api_name:
-	IWTSPlugin.Terminated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWTSPlugin::Terminated


## -description


Notifies the plug-in that the Remote Desktop Connection (RDC) client has terminated. After a call is made to <b>IWTSPlugin::Terminated</b>, no other calls to the plug-in are expected. Any plug-in cleanup should be done here.


## -parameters






## -returns



Returns <b>S_OK</b> if the call completes successfully. Results in no action if the call fails.




## -see-also




<a href="https://msdn.microsoft.com/e34caf2c-1eb6-40eb-9407-20ed4fde9cdb">IWTSPlugin</a>
 

 

