---
UID: NF:tsvirtualchannels.IWTSPlugin.Disconnected
title: IWTSPlugin::Disconnected
author: windows-sdk-content
description: Notifies the plug-in that the Remote Desktop Connection (RDC) client has disconnected from the Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\iwtsplugin_disconnected.htm
tech.root: TermServ
ms.assetid: cbc753b4-531f-476e-8743-b8fbf2481c91
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Disconnected, Disconnected method [Remote Desktop Services], Disconnected method [Remote Desktop Services],IWTSPlugin interface, IWTSPlugin interface [Remote Desktop Services],Disconnected method, IWTSPlugin.Disconnected, IWTSPlugin::Disconnected, termserv.iwtsplugin_disconnected, tsvirtualchannels/IWTSPlugin::Disconnected
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TsVirtualChannels.h
api_name:
 - IWTSPlugin.Disconnected
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSPlugin::Disconnected


## -description


Notifies the plug-in that the Remote Desktop Connection (RDC) client has disconnected from the Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param dwDisconnectCode [in]

Code that identifies the disconnect reason. For the possible codes, see <a href="https://msdn.microsoft.com/f01086e7-61d1-41df-ba0a-4eecfa57d492">IMsTscAxEvents::OnDisconnected</a>.


## -returns



Returns <b>S_OK</b> if the call completes successfully. Results in no action if the call fails.




## -see-also




<a href="https://msdn.microsoft.com/e34caf2c-1eb6-40eb-9407-20ed4fde9cdb">IWTSPlugin</a>
 

 

