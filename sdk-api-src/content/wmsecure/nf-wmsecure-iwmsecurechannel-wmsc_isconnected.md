---
UID: NF:wmsecure.IWMSecureChannel.WMSC_IsConnected
title: IWMSecureChannel::WMSC_IsConnected
author: windows-sdk-content
description: The WMSC_IsConnected method checks to see if the secure connection is valid.
old-location: wmformat\iwmsecurechannel_wmsc_isconnected.htm
old-project: wmformat
ms.assetid: 162bb01f-ba64-4563-a257-28931190ac96
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_IsConnected method, IWMSecureChannel.WMSC_IsConnected, IWMSecureChannel::WMSC_IsConnected, WMSC_IsConnected, WMSC_IsConnected method [windows Media Format], WMSC_IsConnected method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_isconnected, wmsecure/IWMSecureChannel::WMSC_IsConnected
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMT_WATERMARK_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsecure.h
api_name:
 - IWMSecureChannel.WMSC_IsConnected
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSecureChannel::WMSC_IsConnected


## -description


<p class="CCE_Message">[<b>WMSC_IsConnected</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

The <b>WMSC_IsConnected</b> method checks to see if the secure connection is valid.


## -parameters




### -param pfIsConnected [out]

A pointer to value that indicates if the secure connection is valid.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a>
 

 

