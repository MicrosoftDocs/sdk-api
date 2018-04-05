---
UID: NF:wmsecure.IWMSecureChannel.WMSC_Connect
title: IWMSecureChannel::WMSC_Connect method
author: windows-driver-content
description: The WMSC_Connect method initializes the secure connection.
old-location: wmformat\iwmsecurechannel_wmsc_connect.htm
old-project: wmformat
ms.assetid: d8386b23-6319-4687-9de2-a81e661a60e6
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMSecureChannel, IWMSecureChannel interface [windows Media Format], WMSC_Connect method, IWMSecureChannel::WMSC_Connect, WMSC_Connect method [windows Media Format], WMSC_Connect method [windows Media Format], IWMSecureChannel interface, WMSC_Connect,IWMSecureChannel.WMSC_Connect, wmformat.iwmsecurechannel_wmsc_connect, wmsecure/IWMSecureChannel::WMSC_Connect
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMT_WATERMARK_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmsecure.h
api_name:
-	IWMSecureChannel.WMSC_Connect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSecureChannel::WMSC_Connect method


## -description


<p class="CCE_Message">[<b>WMSC_Connect</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

The <b>WMSC_Connect</b> method initializes the secure connection.


## -parameters




### -param pOtherSide [in]

Pointer to a secure channel object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 This function allow each side of the channel to validate the other side before  sharing the secret that will be used for encryption.
    In addition, the DLL serializers used to 
     serialize the encryption become shared.




## -see-also




<a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a>
 

 

