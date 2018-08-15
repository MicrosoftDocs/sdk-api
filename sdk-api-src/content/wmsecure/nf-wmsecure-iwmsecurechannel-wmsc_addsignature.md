---
UID: NF:wmsecure.IWMSecureChannel.WMSC_AddSignature
title: IWMSecureChannel::WMSC_AddSignature
author: windows-sdk-content
description: The WMSC_AddSignature method adds signatures that this object will look for when trying to connect. If no signatures are added, then this object will connect to any other object.
old-location: wmformat\iwmsecurechannel_wmsc_addsignature.htm
old-project: wmformat
ms.assetid: 08fa8ec6-8832-4b5d-bb0d-0a7485ca63d3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_AddSignature method, IWMSecureChannel.WMSC_AddSignature, IWMSecureChannel::WMSC_AddSignature, WMSC_AddSignature, WMSC_AddSignature method [windows Media Format], WMSC_AddSignature method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_addsignature, wmsecure/IWMSecureChannel::WMSC_AddSignature
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsecure.h
req.include-header: 
req.redist: 
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
 - IWMSecureChannel.WMSC_AddSignature
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSecureChannel::WMSC_AddSignature


## -description


<p class="CCE_Message">[<b>WMSC_AddSignature</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

    The <b>WMSC_AddSignature</b> method adds signatures that this object will look for when trying to connect. 
     If no signatures are added, then this object will connect to any other object.


## -parameters




### -param pbCertSig [in]


### -param cbCertSig [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a>
 

 

