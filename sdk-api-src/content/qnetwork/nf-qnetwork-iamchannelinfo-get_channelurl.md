---
UID: NF:qnetwork.IAMChannelInfo.get_ChannelURL
title: IAMChannelInfo::get_ChannelURL
author: windows-sdk-content
description: The get_ChannelURL method retrieves the channel URL.
old-location: dshow\iamchannelinfo_get_channelurl.htm
tech.root: DirectShow
ms.assetid: 27e1a315-db95-4f24-94b6-b10023e61e7a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMChannelInfo interface [DirectShow],get_ChannelURL method, IAMChannelInfo.get_ChannelURL, IAMChannelInfo::get_ChannelURL, IAMChannelInfoget_ChannelURL, dshow.iamchannelinfo_get_channelurl, get_ChannelURL, get_ChannelURL method [DirectShow], get_ChannelURL method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ChannelURL
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMChannelInfo.get_ChannelURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMChannelInfo::get_ChannelURL


## -description



The <code>get_ChannelURL</code> method retrieves the channel URL.




## -parameters




### -param pbstrChannelURL [out]

Pointer to a variable that receives the URL.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/779d1c0a-f838-4d02-8254-d66916d3b790">IAMChannelInfo Interface</a>
 

 

