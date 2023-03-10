---
UID: NF:xenroll.IEnroll.put_ProviderNameWStr
title: IEnroll::put_ProviderNameWStr (xenroll.h)
description: Sets or retrieves the name of the cryptographic service provider (CSP) to use. (Put)
helpviewer_keywords: ["IEnroll interface [Security]","ProviderNameWStr property","IEnroll.ProviderNameWStr","IEnroll.put_ProviderNameWStr","IEnroll::ProviderNameWStr","IEnroll::get_ProviderNameWStr","IEnroll::put_ProviderNameWStr","ProviderNameWStr property [Security]","ProviderNameWStr property [Security]","IEnroll interface","put_ProviderNameWStr","security.ienroll4_providernamewstr","xenroll/IEnroll::ProviderNameWStr","xenroll/IEnroll::get_ProviderNameWStr","xenroll/IEnroll::put_ProviderNameWStr"]
old-location: security\ienroll4_providernamewstr.htm
tech.root: security
ms.assetid: 42300501-2a64-4433-81e9-6ee3fc31b094
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],ProviderNameWStr property, IEnroll.ProviderNameWStr, IEnroll.put_ProviderNameWStr, IEnroll::ProviderNameWStr, IEnroll::get_ProviderNameWStr, IEnroll::put_ProviderNameWStr, ProviderNameWStr property [Security], ProviderNameWStr property [Security],IEnroll interface, put_ProviderNameWStr, security.ienroll4_providernamewstr, xenroll/IEnroll::ProviderNameWStr, xenroll/IEnroll::get_ProviderNameWStr, xenroll/IEnroll::put_ProviderNameWStr
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
 - IEnroll::put_ProviderNameWStr
 - xenroll/IEnroll::put_ProviderNameWStr
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
 - IEnroll.ProviderNameWStr
 - IEnroll.get_ProviderNameWStr
 - IEnroll.put_ProviderNameWStr
---

# IEnroll::put_ProviderNameWStr


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderNameWStr</b> property sets or retrieves the name of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) to use.

If the CSP has not been specified, the default value for this property  is "Microsoft Base Cryptographic Provider", and the <b>ProviderNameWStr</b> property is set to an empty string. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>ProviderNameWStr</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr">createFilePKCS10WStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr">enumContainersWStr</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
