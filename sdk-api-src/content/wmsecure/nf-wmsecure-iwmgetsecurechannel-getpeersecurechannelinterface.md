---
UID: NF:wmsecure.IWMGetSecureChannel.GetPeerSecureChannelInterface
title: IWMGetSecureChannel::GetPeerSecureChannelInterface (wmsecure.h)
author: windows-sdk-content
description: The GetPeerSecureChannelInterface method gets the IWMSecureChannel interface from the other communication party.
old-location: wmformat\iwmgetsecurechannel_getpeersecurechannelinterface.htm
tech.root: wmformat
ms.assetid: bda30638-10b5-4288-b885-b63485606a7f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPeerSecureChannelInterface, GetPeerSecureChannelInterface method [windows Media Format], GetPeerSecureChannelInterface method [windows Media Format],IWMGetSecureChannel interface, IWMGetSecureChannel interface [windows Media Format],GetPeerSecureChannelInterface method, IWMGetSecureChannel.GetPeerSecureChannelInterface, IWMGetSecureChannel::GetPeerSecureChannelInterface, wmformat.iwmgetsecurechannel_getpeersecurechannelinterface, wmsecure/IWMGetSecureChannel::GetPeerSecureChannelInterface
ms.topic: method
req.header: wmsecure.h
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
 - Wmsecure.h
api_name:
 - IWMGetSecureChannel.GetPeerSecureChannelInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMGetSecureChannel::GetPeerSecureChannelInterface


## -description


<p class="CCE_Message">[<b>GetPeerSecureChannelInterface</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

The <b>GetPeerSecureChannelInterface</b> method gets the <a href="https://msdn.microsoft.com/en-us/library/Dd743705(v=VS.85).aspx">IWMSecureChannel</a> interface from the other communication party.


## -parameters




### -param ppPeer [out]

An address of a pointer to the other communication party's <a href="https://msdn.microsoft.com/en-us/library/Dd743705(v=VS.85).aspx">IWMSecureChannel</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798502(v=VS.85).aspx">IWMGetSecureChannel</a>
 

 

