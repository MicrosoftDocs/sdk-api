---
UID: NF:wmsecure.IWMAuthorizer.GetCert
title: IWMAuthorizer::GetCert (wmsecure.h)
author: windows-sdk-content
description: Retrieves the specified certificate.
old-location: wmformat\iwmauthorizer_getcert.htm
tech.root: wmformat
ms.assetid: e165356c-b14b-47dc-b046-a74499251cab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCert, GetCert method [windows Media Format], GetCert method [windows Media Format],IWMAuthorizer interface, IWMAuthorizer interface [windows Media Format],GetCert method, IWMAuthorizer.GetCert, IWMAuthorizer::GetCert, wmformat.iwmauthorizer_getcert, wmsecure/IWMAuthorizer::GetCert
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
 - IWMAuthorizer.GetCert
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMAuthorizer::GetCert


## -description


<p class="CCE_Message">[<b>GetCert</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

Retrieves the specified certificate.


## -parameters




### -param dwIndex [in]

The index of the certification to retrieve.


### -param ppbCertData [out]

An address of a pointer to certification data. <i>ppbCertData</i> is allocated with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and must be released by the user.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743287(v=VS.85).aspx">IWMAuthorizer</a>
 

 

