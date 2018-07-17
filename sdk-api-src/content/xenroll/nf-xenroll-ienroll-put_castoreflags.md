---
UID: NF:xenroll.IEnroll.put_CAStoreFlags
title: IEnroll::put_CAStoreFlags
author: windows-sdk-content
description: The CAStoreFlags property of IEnroll4 sets or retrieves a flag that controls the certification authority (CA) store when the store is opened.
old-location: security\ienroll4_castoreflags.htm
old-project: SecCrypto
ms.assetid: 294a8a38-9c76-4e5c-ac11-2fcb8b81727e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CAStoreFlags property [Security], CAStoreFlags property [Security],IEnroll interface, IEnroll interface [Security],CAStoreFlags property, IEnroll.CAStoreFlags, IEnroll.put_CAStoreFlags, IEnroll::CAStoreFlags, IEnroll::get_CAStoreFlags, IEnroll::put_CAStoreFlags, put_CAStoreFlags, security.ienroll4_castoreflags, xenroll/IEnroll::CAStoreFlags, xenroll/IEnroll::get_CAStoreFlags, xenroll/IEnroll::put_CAStoreFlags
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.CAStoreFlags
 - IEnroll.get_CAStoreFlags
 - IEnroll.put_CAStoreFlags
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::put_CAStoreFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>CAStoreFlags</b> property sets or retrieves a flag that controls the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) store when the store is opened. This flag is  passed to the <i>dwFlags</i> parameter of the <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> function when the CA store is opened.

The default value for this property is CERT_SYSTEM_STORE_CURRENT_USER.  This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>CAStoreFlags</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/8772f528-2c33-48f4-bb0c-cfde91cf2fba">acceptPKCS7Blob</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c2b99df-769b-457b-b5c5-7690b73d6f84">acceptFilePKCS7WStr</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

