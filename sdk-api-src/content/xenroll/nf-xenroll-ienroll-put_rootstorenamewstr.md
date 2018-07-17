---
UID: NF:xenroll.IEnroll.put_RootStoreNameWStr
title: IEnroll::put_RootStoreNameWStr
author: windows-sdk-content
description: The RootStoreNameWStr property of IEnroll4 sets or retrieves the name of the root store where all intrinsically trusted, self-signed root certificates are kept.
old-location: security\ienroll4_rootstorenamewstr.htm
old-project: SecCrypto
ms.assetid: d1b60ba4-974e-43d4-a8f9-8ca619d6b878
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IEnroll interface [Security],RootStoreNameWStr property, IEnroll.RootStoreNameWStr, IEnroll.put_RootStoreNameWStr, IEnroll::RootStoreNameWStr, IEnroll::get_RootStoreNameWStr, IEnroll::put_RootStoreNameWStr, RootStoreNameWStr property [Security], RootStoreNameWStr property [Security],IEnroll interface, put_RootStoreNameWStr, security.ienroll4_rootstorenamewstr, xenroll/IEnroll::RootStoreNameWStr, xenroll/IEnroll::get_RootStoreNameWStr, xenroll/IEnroll::put_RootStoreNameWStr
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
 - IEnroll.RootStoreNameWStr
 - IEnroll.get_RootStoreNameWStr
 - IEnroll.put_RootStoreNameWStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::put_RootStoreNameWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RootStoreNameWStr</b> property sets or retrieves the name of the root store where all intrinsically trusted, self-signed <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">root certificates</a> are kept.

 The default value for this property is "ROOT". Because of the level of trust associated with the root store, the user may be prompted (by means of the user interface) to accept the certificate. Although this property need not be changed for many applications, to avoid the user interface associated with trusting <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">root certificates</a>, a possibility is to set <b>RootStoreNameWStr</b> to "CA".

This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




<b>RootStoreNameWStr</b> affects the behavior of the following methods:

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
 

 

