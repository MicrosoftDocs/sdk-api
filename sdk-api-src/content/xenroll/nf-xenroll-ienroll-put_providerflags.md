---
UID: NF:xenroll.IEnroll.put_ProviderFlags
title: IEnroll::put_ProviderFlags
author: windows-sdk-content
description: The ProviderFlags property of IEnroll4 sets or retrieves the provider type.
old-location: security\ienroll4_providerflags.htm
tech.root: seccrypto
ms.assetid: 57e6f86e-fbd3-4fd7-acdd-146a67045ff8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnroll interface [Security],ProviderFlags property, IEnroll.ProviderFlags, IEnroll.put_ProviderFlags, IEnroll::ProviderFlags, IEnroll::get_ProviderFlags, IEnroll::put_ProviderFlags, ProviderFlags property [Security], ProviderFlags property [Security],IEnroll interface, put_ProviderFlags, security.ienroll4_providerflags, xenroll/IEnroll::ProviderFlags, xenroll/IEnroll::get_ProviderFlags, xenroll/IEnroll::put_ProviderFlags
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.ProviderFlags
 - IEnroll.get_ProviderFlags
 - IEnroll.put_ProviderFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::put_ProviderFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderFlags</b> property  sets or retrieves the provider type.

The <b>ProviderFlags</b> property is passed to the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> CryptoAPI function. Valid values are determined by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) in use.

The default value for this property is zero. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



For  more information about   valid <b>ProviderFlags</b> values for the Microsoft Base Cryptographic Provider, see the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> CryptoAPI function.

For information about  other CSPs, see the documentation provided with the CSP.

The <b>ProviderFlags</b> property value is passed to <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>  by using  its <i>dwFlags</i> parameter.


The <b>ProviderFlags</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

