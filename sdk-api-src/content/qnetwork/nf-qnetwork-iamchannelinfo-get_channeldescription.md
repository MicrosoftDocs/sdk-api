---
UID: NF:qnetwork.IAMChannelInfo.get_ChannelDescription
title: IAMChannelInfo::get_ChannelDescription
author: windows-sdk-content
description: The get_ChannelDescription method retrieves the description of the channel.
old-location: dshow\iamchannelinfo_get_channeldescription.htm
old-project: DirectShow
ms.assetid: c39b15af-0766-4512-9720-4cdaef6120ba
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IAMChannelInfo interface [DirectShow],get_ChannelDescription method, IAMChannelInfo.get_ChannelDescription, IAMChannelInfo::get_ChannelDescription, IAMChannelInfoget_ChannelDescription, dshow.iamchannelinfo_get_channeldescription, get_ChannelDescription, get_ChannelDescription method [DirectShow], get_ChannelDescription method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ChannelDescription
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMChannelInfo.get_ChannelDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAMChannelInfo::get_ChannelDescription


## -description



The <code>get_ChannelDescription</code> method retrieves the description of the channel.




## -parameters




### -param pbstrChannelDescription [out]

Receives the channel description.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/779d1c0a-f838-4d02-8254-d66916d3b790">IAMChannelInfo Interface</a>
 

 

