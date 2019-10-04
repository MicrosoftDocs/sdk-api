---
UID: NF:xenroll.IEnroll.put_UseExistingKeySet
title: IEnroll::put_UseExistingKeySet (xenroll.h)
author: windows-sdk-content
description: The UseExistingKeySet property of IEnroll4 sets or retrieves a Boolean value that determines whether the existing keys should be used.
old-location: security\ienroll4_useexistingkeyset.htm
tech.root: SecCrypto
ms.assetid: 1534ec57-71d3-4189-a94e-7bcb3c0670e1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],UseExistingKeySet property, IEnroll.UseExistingKeySet, IEnroll.put_UseExistingKeySet, IEnroll::UseExistingKeySet, IEnroll::get_UseExistingKeySet, IEnroll::put_UseExistingKeySet, UseExistingKeySet property [Security], UseExistingKeySet property [Security],IEnroll interface, put_UseExistingKeySet, security.ienroll4_useexistingkeyset, xenroll/IEnroll::UseExistingKeySet, xenroll/IEnroll::get_UseExistingKeySet, xenroll/IEnroll::put_UseExistingKeySet
ms.topic: method
f1_keywords: 
 - "xenroll/IEnroll.UseExistingKeySet"
dev_langs:
 - c++
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
 - IEnroll.UseExistingKeySet
 - IEnroll.get_UseExistingKeySet
 - IEnroll.put_UseExistingKeySet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll::put_UseExistingKeySet


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>UseExistingKeySet</b> property  sets or retrieves a Boolean value that determines whether the existing keys should be used.

This property was first defined in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



 If an existing key set is used, the <b>UseExistingKeySet</b> property must be set to true.


The <b>UseExistingKeySet</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr">createFilePKCS10WStr</a>
</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
 

 

