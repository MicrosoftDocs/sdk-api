---
UID: NF:wmpservices.IWMPPlugin.UnAdviseWMPServices
title: IWMPPlugin::UnAdviseWMPServices method
author: windows-driver-content
description: The IWMPPlugin::UnAdviseWMPServices method is used to release the pointer provided by AdviseWMPServices.
old-location: wmp\iwmpplugin_unadvisewmpservices.htm
old-project: WMP
ms.assetid: 377a6853-94fb-4467-a893-508b56637a16
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPPlugin, IWMPPlugin interface [Windows Media Player], UnAdviseWMPServices method, IWMPPlugin::UnAdviseWMPServices, IWMPPluginUnAdviseWMPServicesDSP, UnAdviseWMPServices method [Windows Media Player], UnAdviseWMPServices method [Windows Media Player], IWMPPlugin interface, UnAdviseWMPServices,IWMPPlugin.UnAdviseWMPServices, wmp.iwmpplugin_unadvisewmpservices, wmpservices/IWMPPlugin::UnAdviseWMPServices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WMPServices_StreamState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmpservices.h
api_name:
-	IWMPPlugin.UnAdviseWMPServices
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlugin::UnAdviseWMPServices method


## -description



The <b>IWMPPlugin::UnAdviseWMPServices</b> method is used to release the pointer provided by <b>AdviseWMPServices</b>.




## -parameters






## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Windows Media Player calls this method when the pointer provided by <b>AdviseWMPServices</b> is no longer valid. The plug-in should use this method to cease making stream state requests through the pointer.




## -see-also




<a href="https://msdn.microsoft.com/e384aa43-72ab-44b7-b6bd-7a29335b5197">IWMPPlugin Interface</a>



<a href="https://msdn.microsoft.com/203b9363-1363-48be-8ba6-8b152ae9a92f">IWMPPlugin::AdviseWMPServices</a>
 

 

