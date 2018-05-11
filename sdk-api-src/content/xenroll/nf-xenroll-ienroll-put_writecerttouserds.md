---
UID: NF:xenroll.IEnroll.put_WriteCertToUserDS
title: IEnroll::put_WriteCertToUserDS
author: windows-driver-content
description: The WriteCertToUserDS property of IEnroll4 sets or retrieves a Boolean value that determines whether the certificate is written to the user's Active Directory store.
old-location: security\ienroll4_writecerttouserds.htm
old-project: SecCrypto
ms.assetid: 8b29f442-265f-4826-a2f0-3305d6f70cbb
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IEnroll interface [Security],WriteCertToUserDS property, IEnroll.WriteCertToUserDS, IEnroll.put_WriteCertToUserDS, IEnroll::WriteCertToUserDS, IEnroll::get_WriteCertToUserDS, IEnroll::put_WriteCertToUserDS, WriteCertToUserDS property [Security], WriteCertToUserDS property [Security],IEnroll interface, put_WriteCertToUserDS, security.ienroll4_writecerttouserds, xenroll/IEnroll::WriteCertToUserDS, xenroll/IEnroll::get_WriteCertToUserDS, xenroll/IEnroll::put_WriteCertToUserDS
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
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xenroll.dll
api_name:
-	IEnroll.WriteCertToUserDS
-	IEnroll.get_WriteCertToUserDS
-	IEnroll.put_WriteCertToUserDS
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::put_WriteCertToUserDS


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WriteCertToUserDS</b> property sets or retrieves a Boolean value that determines whether the certificate is written to the user's Active Directory  store.

 This property should not need to be modified by most applications. This property was first defined in the <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a> interface.

This property is read/write.


## -parameters


## -remarks




<b>WriteCertToUserDS</b> affects the behavior of the following methods:

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
 

 

