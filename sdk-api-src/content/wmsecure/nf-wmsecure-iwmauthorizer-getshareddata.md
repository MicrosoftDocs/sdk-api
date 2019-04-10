---
UID: NF:wmsecure.IWMAuthorizer.GetSharedData
title: IWMAuthorizer::GetSharedData (wmsecure.h)
author: windows-sdk-content
description: Retrieves shared data for the specified certificate.
old-location: wmformat\iwmauthorizer_getshareddata.htm
tech.root: wmformat
ms.assetid: 575df33a-b29e-43eb-84c2-6f9875f26196
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSharedData, GetSharedData method [windows Media Format], GetSharedData method [windows Media Format],IWMAuthorizer interface, IWMAuthorizer interface [windows Media Format],GetSharedData method, IWMAuthorizer.GetSharedData, IWMAuthorizer::GetSharedData, wmformat.iwmauthorizer_getshareddata, wmsecure/IWMAuthorizer::GetSharedData
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
 - IWMAuthorizer.GetSharedData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMAuthorizer::GetSharedData


## -description


<p class="CCE_Message">[<b>GetSharedData</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

Retrieves shared  data for the specified certificate.


## -parameters




### -param dwCertIndex [in]


### -param pbSharedData [in]


### -param pbCert [in]


### -param ppbSharedData [out]

An address of a pointer to certification data. <i>ppbCertData</i> is allocated with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and must be released by the user.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743287(v=VS.85).aspx">IWMAuthorizer</a>
 

 

