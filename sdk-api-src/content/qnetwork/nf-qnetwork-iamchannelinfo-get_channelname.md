---
UID: NF:qnetwork.IAMChannelInfo.get_ChannelName
title: IAMChannelInfo::get_ChannelName method
author: windows-driver-content
description: The get_ChannelName method retrieves the channel name.
old-location: dshow\iamchannelinfo_get_channelname.htm
old-project: DirectShow
ms.assetid: 6cf4f8aa-d6aa-46bd-83b1-fba762fbb8bb
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IAMChannelInfo, IAMChannelInfo interface [DirectShow], get_ChannelName method, IAMChannelInfo::get_ChannelName, IAMChannelInfoget_ChannelName, dshow.iamchannelinfo_get_channelname, get_ChannelName method [DirectShow], get_ChannelName method [DirectShow], IAMChannelInfo interface, get_ChannelName,IAMChannelInfo.get_ChannelName, qnetwork/IAMChannelInfo::get_ChannelName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Qnetwork.h
api_name:
-	IAMChannelInfo.get_ChannelName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IAMChannelInfo::get_ChannelName method


## -description



The <code>get_ChannelName</code> method retrieves the channel name.




## -parameters




### -param pbstrChannelName [out]

Pointer to a variable that receives a string containing the channel name.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/779d1c0a-f838-4d02-8254-d66916d3b790">IAMChannelInfo Interface</a>
 

 

