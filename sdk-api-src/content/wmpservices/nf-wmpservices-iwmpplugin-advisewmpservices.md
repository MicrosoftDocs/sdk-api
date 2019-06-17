---
UID: NF:wmpservices.IWMPPlugin.AdviseWMPServices
title: IWMPPlugin::AdviseWMPServices (wmpservices.h)
author: windows-sdk-content
description: The IWMPPlugin::AdviseWMPServices method is implemented by the plug-in.
old-location: wmp\iwmpplugin_advisewmpservices.htm
tech.root: WMP
ms.assetid: 203b9363-1363-48be-8ba6-8b152ae9a92f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AdviseWMPServices, AdviseWMPServices method [Windows Media Player], AdviseWMPServices method [Windows Media Player],IWMPPlugin interface, IWMPPlugin interface [Windows Media Player],AdviseWMPServices method, IWMPPlugin.AdviseWMPServices, IWMPPlugin::AdviseWMPServices, IWMPPluginAdviseWMPServicesDSP, wmp.iwmpplugin_advisewmpservices, wmpservices/IWMPPlugin::AdviseWMPServices
ms.topic: method
f1_keywords: ["wmpservices/IWMPPlugin.AdviseWMPServices"]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPPlugin.AdviseWMPServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlugin::AdviseWMPServices


## -description



The <b>IWMPPlugin::AdviseWMPServices</b> method is implemented by the plug-in.




## -parameters




### -param pWMPServices [in]

Pointer to an <b>IWMPServices</b> interface.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Windows Media Player calls the <b>AdviseWMPServices</b> method on the plug-in to pass in a pointer that the plug-in can then use to call the <b>IWMPServices</b> interface, which contains methods that provide information about the current state of the stream.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin">IWMPPlugin Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices">IWMPServices Interface</a>
 

 

