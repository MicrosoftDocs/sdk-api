---
UID: NF:xenroll.IEnroll.put_CAStoreNameWStr
title: IEnroll::put_CAStoreNameWStr (xenroll.h)
author: windows-sdk-content
description: The CAStoreNameWStr property of IEnroll4 sets or retrieves the name of the store where all non-&#0034;ROOT&#0034; and non-&#0034;MY&#0034; certificates are kept.
old-location: security\ienroll4_castorenamewstr.htm
tech.root: SecCrypto
ms.assetid: 4c016649-a780-45c1-94a4-fb08c15c4e0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CAStoreNameWStr property [Security], CAStoreNameWStr property [Security],IEnroll interface, IEnroll interface [Security],CAStoreNameWStr property, IEnroll.CAStoreNameWStr, IEnroll.put_CAStoreNameWStr, IEnroll::CAStoreNameWStr, IEnroll::get_CAStoreNameWStr, IEnroll::put_CAStoreNameWStr, put_CAStoreNameWStr, security.ienroll4_castorenamewstr, xenroll/IEnroll::CAStoreNameWStr, xenroll/IEnroll::get_CAStoreNameWStr, xenroll/IEnroll::put_CAStoreNameWStr
ms.topic: method
f1_keywords: 
 - "xenroll/IEnroll.CAStoreNameWStr"
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
 - IEnroll.CAStoreNameWStr
 - IEnroll.get_CAStoreNameWStr
 - IEnroll.put_CAStoreNameWStr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll::put_CAStoreNameWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>CAStoreNameWStr</b> property  sets or retrieves the name of the store where all non-"ROOT" and non-"MY" certificates are kept.

The default value for this property is "CA". This property was first defined in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>CAStoreNameWStr</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr">acceptFilePKCS7WStr</a>
</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
 

 

