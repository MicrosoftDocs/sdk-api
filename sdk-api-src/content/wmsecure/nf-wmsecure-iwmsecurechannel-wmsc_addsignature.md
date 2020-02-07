---
UID: NF:wmsecure.IWMSecureChannel.WMSC_AddSignature
title: IWMSecureChannel::WMSC_AddSignature (wmsecure.h)
description: The WMSC_AddSignature method adds signatures that this object will look for when trying to connect. If no signatures are added, then this object will connect to any other object.
old-location: wmformat\iwmsecurechannel_wmsc_addsignature.htm
tech.root: wmformat
ms.assetid: 08fa8ec6-8832-4b5d-bb0d-0a7485ca63d3
ms.date: 12/05/2018
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_AddSignature method, IWMSecureChannel.WMSC_AddSignature, IWMSecureChannel::WMSC_AddSignature, WMSC_AddSignature, WMSC_AddSignature method [windows Media Format], WMSC_AddSignature method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_addsignature, wmsecure/IWMSecureChannel::WMSC_AddSignature
f1_keywords:
- wmsecure/IWMSecureChannel.WMSC_AddSignature
dev_langs:
- c++
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
- IWMSecureChannel.WMSC_AddSignature
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSecureChannel::WMSC_AddSignature


## -description


<p class="CCE_Message">[<b>WMSC_AddSignature</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

    The <b>WMSC_AddSignature</b> method adds signatures that this object will look for when trying to connect. 
     If no signatures are added, then this object will connect to any other object.


## -parameters




### -param pbCertSig [in]


### -param cbCertSig [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>
 

 

