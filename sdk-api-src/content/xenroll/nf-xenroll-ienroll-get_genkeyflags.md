---
UID: NF:xenroll.IEnroll.get_GenKeyFlags
title: IEnroll::get_GenKeyFlags
author: windows-sdk-content
description: Sets or retrieves the values passed to CryptGenKey when the certificate request is generated.
old-location: security\ienroll4_genkeyflags.htm
tech.root: seccrypto
ms.assetid: 6dac3321-9dca-4b7d-8432-e8124bd51db7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GenKeyFlags property [Security], GenKeyFlags property [Security],IEnroll interface, IEnroll interface [Security],GenKeyFlags property, IEnroll.GenKeyFlags, IEnroll.get_GenKeyFlags, IEnroll::GenKeyFlags, IEnroll::get_GenKeyFlags, IEnroll::put_GenKeyFlags, get_GenKeyFlags, security.ienroll4_genkeyflags, xenroll/IEnroll::GenKeyFlags, xenroll/IEnroll::get_GenKeyFlags, xenroll/IEnroll::put_GenKeyFlags
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IEnroll.GenKeyFlags
 - IEnroll.get_GenKeyFlags
 - IEnroll.put_GenKeyFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::get_GenKeyFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GenKeyFlags</b> property sets or retrieves the values passed to <a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a> when the certificate request is generated.

By default, the <b>GenKeyFlags</b> property is set to zero. However, when a .pvk file is specified, the value of <b>GenKeyFlags</b> defaults to CRYPT_EXPORTABLE. For more information, see Remarks.

This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



By default, private keys are not exportable unless a .pvk file is requested. To make the private key exportable without specifying a .pvk file, set <b>GenKeyFlags</b> to CRYPT_EXPORTABLE.

To specify a .pvk file name,  use the 
<a href="https://msdn.microsoft.com/5518c252-fdca-444b-b87e-9fe3cb3b3e3f">PVKFileNameWStr</a> property.

The <b>GenKeyFlags</b> property value is passed to the 
<a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a> CryptoAPI function by using its <i>dwFlags</i> parameter.

If the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a>  (CSP) does not support exportable private keys, an error occurs.


The <b>GenKeyFlags</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bc2b875c-96f8-453e-8f72-f9032d5aa773">createRequestWStr</a>
</li>
</ul>


<div class="alert"><b>Note</b>  The default value for the <b>GenKeyFlags</b> property is zero. If you need to change this value, you must do so before calling these methods. After calling any of these methods, you cannot change the <b>GenKeyFlags</b> property value.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a>



<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

