---
UID: NF:wmsecure.IWMSecureChannel.WMSC_GetValidCertificate
title: IWMSecureChannel::WMSC_GetValidCertificate
author: windows-sdk-content
description: The WMSC_GetValidCertificate method returns a copy of the certificate that was used provided by the other side of the connection. Also returns the index of the signature that validated that certificate.
old-location: wmformat\iwmsecurechannel_wmsc_getvalidcertificate.htm
tech.root: wmformat
ms.assetid: 0ecc25c5-238e-4415-952e-7d830ba1c317
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_GetValidCertificate method, IWMSecureChannel.WMSC_GetValidCertificate, IWMSecureChannel::WMSC_GetValidCertificate, WMSC_GetValidCertificate, WMSC_GetValidCertificate method [windows Media Format], WMSC_GetValidCertificate method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_getvalidcertificate, wmsecure/IWMSecureChannel::WMSC_GetValidCertificate
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
 - IWMSecureChannel.WMSC_GetValidCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSecureChannel::WMSC_GetValidCertificate


## -description


<p class="CCE_Message">[<b>WMSC_GetValidCertificate</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

The <b>WMSC_GetValidCertificate</b> method returns a copy of the certificate that was used provided by the other side
     of the connection.   Also returns the index of the signature that validated
     that certificate.  


## -parameters




### -param ppbCertificate [out]

<i>ppbCertificate</i> must be released with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> by the user.
     <i>ppbCertificate</i> can be <b>NULL</b> if no certificate was provided. 
     If no connection was made, this function returns E_FAIL


### -param pdwSignature [out]

<i>pdwSignature</i>can be 0xFFFFFFFF if no signature was used to validate the cert.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743705(v=VS.85).aspx">IWMSecureChannel</a>
 

 

