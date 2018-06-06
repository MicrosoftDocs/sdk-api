---
UID: NF:wmsecure.IWMAuthorizer.GetCertCount
title: IWMAuthorizer::GetCertCount
author: windows-sdk-content
description: Get the number of certificates.
old-location: wmformat\iwmauthorizer_getcertcount.htm
old-project: wmformat
ms.assetid: afe8a924-3d2b-42e6-9700-a6075f51ff10
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetCertCount, GetCertCount method [windows Media Format], GetCertCount method [windows Media Format],IWMAuthorizer interface, IWMAuthorizer interface [windows Media Format],GetCertCount method, IWMAuthorizer.GetCertCount, IWMAuthorizer::GetCertCount, wmformat.iwmauthorizer_getcertcount, wmsecure/IWMAuthorizer::GetCertCount
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
 - IWMAuthorizer.GetCertCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMAuthorizer::GetCertCount


## -description


<p class="CCE_Message">[<b>GetCertCount</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

Get the number of certificates.


## -parameters




### -param pcCerts [out]

Receives a pointer to a count of certs.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/eece7e36-7c3e-4bc4-9b5a-8142a062dbce">IWMAuthorizer</a>
 

 

