---
UID: NF:xenroll.IEnroll.put_ContainerNameWStr
title: IEnroll::put_ContainerNameWStr (xenroll.h)
description: Sets or retrieves the name of the key container to use. (Put)
helpviewer_keywords: ["ContainerNameWStr property [Security]","ContainerNameWStr property [Security]","IEnroll interface","IEnroll interface [Security]","ContainerNameWStr property","IEnroll.ContainerNameWStr","IEnroll.put_ContainerNameWStr","IEnroll::ContainerNameWStr","IEnroll::get_ContainerNameWStr","IEnroll::put_ContainerNameWStr","put_ContainerNameWStr","security.ienroll4_containernamewstr","xenroll/IEnroll::ContainerNameWStr","xenroll/IEnroll::get_ContainerNameWStr","xenroll/IEnroll::put_ContainerNameWStr"]
old-location: security\ienroll4_containernamewstr.htm
tech.root: security
ms.assetid: 6740378a-342b-4520-89c7-32d44e23cfca
ms.date: 12/05/2018
ms.keywords: ContainerNameWStr property [Security], ContainerNameWStr property [Security],IEnroll interface, IEnroll interface [Security],ContainerNameWStr property, IEnroll.ContainerNameWStr, IEnroll.put_ContainerNameWStr, IEnroll::ContainerNameWStr, IEnroll::get_ContainerNameWStr, IEnroll::put_ContainerNameWStr, put_ContainerNameWStr, security.ienroll4_containernamewstr, xenroll/IEnroll::ContainerNameWStr, xenroll/IEnroll::get_ContainerNameWStr, xenroll/IEnroll::put_ContainerNameWStr
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
 - IEnroll::put_ContainerNameWStr
 - xenroll/IEnroll::put_ContainerNameWStr
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
 - IEnroll.ContainerNameWStr
 - IEnroll.get_ContainerNameWStr
 - IEnroll.put_ContainerNameWStr
---

# IEnroll::put_ContainerNameWStr


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ContainerNameWStr</b> property sets or retrieves the  name of the <a href="/windows/desktop/SecGloss/k-gly">key container</a> to use.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The container specified may be an existing container or a new one. It may only be an existing container if the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset">UseExistingKeySet</a> property is set, as long as the key set has not been generated yet. For example, if only an <a href="/windows/desktop/SecGloss/e-gly">exchange key</a> set has been generated for a container, it is still possible to perform a certificate enrollment using the signature key set without setting <b>UseExistingKeySet</b>. The <i>exchange key set</i> could be used if <b>UseExistingKeySet</b> is set beforehand.

By default, a new container is selected each time the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> control is run. This ensures that a new key set is generated. If this property is not explicitly set, a generated GUID is used as the container name.


The <b>ContainerNameWStr</b> property affects the behavior of the following methods:

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
