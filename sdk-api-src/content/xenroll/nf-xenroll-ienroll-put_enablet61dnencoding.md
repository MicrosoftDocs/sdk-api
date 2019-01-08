---
UID: NF:xenroll.IEnroll.put_EnableT61DNEncoding
title: IEnroll::put_EnableT61DNEncoding
author: windows-sdk-content
description: Sets or retrieves a Boolean value that determines whether the distinguished name in the request is encoded as a T61 string instead of as a Unicode string.
old-location: security\ienroll4_enablet61dnencoding.htm
tech.root: SecCrypto
ms.assetid: 7ed181d1-b06f-40f4-892a-80edf327bf40
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnableT61DNEncoding property [Security], EnableT61DNEncoding property [Security],IEnroll interface, IEnroll interface [Security],EnableT61DNEncoding property, IEnroll.EnableT61DNEncoding, IEnroll.put_EnableT61DNEncoding, IEnroll::EnableT61DNEncoding, IEnroll::get_EnableT61DNEncoding, IEnroll::put_EnableT61DNEncoding, put_EnableT61DNEncoding, security.ienroll4_enablet61dnencoding, xenroll/IEnroll::EnableT61DNEncoding, xenroll/IEnroll::get_EnableT61DNEncoding, xenroll/IEnroll::put_EnableT61DNEncoding
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
 - IEnroll.EnableT61DNEncoding
 - IEnroll.get_EnableT61DNEncoding
 - IEnroll.put_EnableT61DNEncoding
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::put_EnableT61DNEncoding


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>EnableT61DNEncoding</b> property sets or retrieves a Boolean value that determines whether the distinguished name in the request is encoded as a T61 string instead of as a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> string.

 A T61 character is 8 bits, hence all <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> characters to be encoded must be less than or equal to 0xFF.  This property was first defined in the <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>EnableT61DNEncoding</b> property affects the behavior of the following methods:

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
 

 

