---
UID: NF:xenroll.IEnroll.get_PVKFileNameWStr
title: IEnroll::get_PVKFileNameWStr (xenroll.h)
description: Sets or retrieves the name of the file that will contain exported keys. (Get)
helpviewer_keywords: ["IEnroll interface [Security]","PVKFileNameWStr property","IEnroll.PVKFileNameWStr","IEnroll.get_PVKFileNameWStr","IEnroll::PVKFileNameWStr","IEnroll::get_PVKFileNameWStr","IEnroll::put_PVKFileNameWStr","PVKFileNameWStr property [Security]","PVKFileNameWStr property [Security]","IEnroll interface","get_PVKFileNameWStr","security.ienroll4_pvkfilenamewstr","xenroll/IEnroll::PVKFileNameWStr","xenroll/IEnroll::get_PVKFileNameWStr","xenroll/IEnroll::put_PVKFileNameWStr"]
old-location: security\ienroll4_pvkfilenamewstr.htm
tech.root: security
ms.assetid: 5518c252-fdca-444b-b87e-9fe3cb3b3e3f
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],PVKFileNameWStr property, IEnroll.PVKFileNameWStr, IEnroll.get_PVKFileNameWStr, IEnroll::PVKFileNameWStr, IEnroll::get_PVKFileNameWStr, IEnroll::put_PVKFileNameWStr, PVKFileNameWStr property [Security], PVKFileNameWStr property [Security],IEnroll interface, get_PVKFileNameWStr, security.ienroll4_pvkfilenamewstr, xenroll/IEnroll::PVKFileNameWStr, xenroll/IEnroll::get_PVKFileNameWStr, xenroll/IEnroll::put_PVKFileNameWStr
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
 - IEnroll::get_PVKFileNameWStr
 - xenroll/IEnroll::get_PVKFileNameWStr
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
 - IEnroll.PVKFileNameWStr
 - IEnroll.get_PVKFileNameWStr
 - IEnroll.put_PVKFileNameWStr
---

# IEnroll::get_PVKFileNameWStr


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>PVKFileNameWStr</b> property sets or retrieves the name of the file that will contain exported keys.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>PVKFileNameWStr</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr">createFilePKCS10WStr</a>
</li>
</ul>


Exporting functionality may not be supported by the  <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). Historically, <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> has exported the <a href="/windows/desktop/SecGloss/p-gly">private key</a> to a .pvk file on a disk and removed the keys from the registry. By default, private keys are not generated for exportation, and many cryptographic service providers do not support exporting keys. However, if the CSP supports exporting private keys, specifying a non-NULL value for the <b>PVKFileNameWStr</b> property causes the private keys to be generated as exportable and the private and public keys to be written to the file specified by the <b>PVKFileNameWStr</b> property. The private key is removed from the CSP. The file name specified by the property can be any accessible file. By default, no .pvk file is generated, and the keys are not generated as exportable.

If the .pvk file already exists, the user is notified and prompted for permission to overwrite it.


The 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">GenKeyFlags</a> property also has a flag that controls whether the private key can be exported. Use care when using  the <b>GenKeyFlags</b> property and the <b>PVKFileNameWStr</b> property together. If the <b>PVKFileNameWStr</b> property is set first, the <b>GenKeyFlags</b> property is automatically set to CRYPT_EXPORTABLE. If the <b>GenKeyFlags</b> property is set (by using the <b>put_GenKeyFlags</b> function) without including the CRYPT_EXPORTABLE flag, then the <b>GenKeyFlags</b> will not be set to CRYPT_EXPORTABLE, and the generated keys will not be exportable. The following procedure demonstrates this:

<ol>
<li>Call <b>put_PVKFileNameWStr</b> to set the file name for the file that will receive the exported keys. The <a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">GenKeyFlags</a> property is automatically set to CRYPT_EXPORTABLE.</li>
<li>Call <a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">put_GenKeyFlags</a> with a value not set to CRYPT_EXPORTABLE, for example, zero.</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">GenKeyFlags</a> is no longer set to CRYPT_EXPORTABLE (the value that was automatically set in step one).</li>
</ol>


Any keys generated by following the previous steps will be not exportable. Therefore, it is recommended that the user set the <a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">GenKeyFlags</a> property before the <b>PVKFileNameWStr</b> property when they are used together.

Alternatively, the user could determine the current value of the CRYPT_EXPORTABLE bit in the <a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">GenKeyFlags</a> property and then perform a bitwise-<b>OR</b>  operation between this value and any changes that are made to the <b>GenKeyFlags</b> property to ensure that the bit is not wiped out. The user could also specifically set the CRYPT_EXPORTABLE bit when updating the <b>GenKeyFlags</b> property.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
