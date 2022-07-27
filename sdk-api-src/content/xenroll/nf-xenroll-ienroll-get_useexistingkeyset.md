---
UID: NF:xenroll.IEnroll.get_UseExistingKeySet
title: IEnroll::get_UseExistingKeySet (xenroll.h)
description: The UseExistingKeySet property of IEnroll4 sets or retrieves a Boolean value that determines whether the existing keys should be used. (Get)
helpviewer_keywords: ["IEnroll interface [Security]","UseExistingKeySet property","IEnroll.UseExistingKeySet","IEnroll.get_UseExistingKeySet","IEnroll::UseExistingKeySet","IEnroll::get_UseExistingKeySet","IEnroll::put_UseExistingKeySet","UseExistingKeySet property [Security]","UseExistingKeySet property [Security]","IEnroll interface","get_UseExistingKeySet","security.ienroll4_useexistingkeyset","xenroll/IEnroll::UseExistingKeySet","xenroll/IEnroll::get_UseExistingKeySet","xenroll/IEnroll::put_UseExistingKeySet"]
old-location: security\ienroll4_useexistingkeyset.htm
tech.root: security
ms.assetid: 1534ec57-71d3-4189-a94e-7bcb3c0670e1
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],UseExistingKeySet property, IEnroll.UseExistingKeySet, IEnroll.get_UseExistingKeySet, IEnroll::UseExistingKeySet, IEnroll::get_UseExistingKeySet, IEnroll::put_UseExistingKeySet, UseExistingKeySet property [Security], UseExistingKeySet property [Security],IEnroll interface, get_UseExistingKeySet, security.ienroll4_useexistingkeyset, xenroll/IEnroll::UseExistingKeySet, xenroll/IEnroll::get_UseExistingKeySet, xenroll/IEnroll::put_UseExistingKeySet
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnroll::get_UseExistingKeySet
 - xenroll/IEnroll::get_UseExistingKeySet
dev_langs:
 - c++
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
---

# IEnroll::get_UseExistingKeySet


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>UseExistingKeySet</b> property  sets or retrieves a Boolean value that determines whether the existing keys should be used.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

 If an existing key set is used, the <b>UseExistingKeySet</b> property must be set to true.


The <b>UseExistingKeySet</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr">createFilePKCS10WStr</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
