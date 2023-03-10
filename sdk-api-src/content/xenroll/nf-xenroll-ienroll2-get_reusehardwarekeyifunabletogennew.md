---
UID: NF:xenroll.IEnroll2.get_ReuseHardwareKeyIfUnableToGenNew
title: IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew (xenroll.h)
description: The ReuseHardwareKeyIfUnableToGenNew property of IEnroll4 sets or retrieves a Boolean value that determines the action taken by the certificate enrollment control object if an error is encountered when generating a new key. (Get)
helpviewer_keywords: ["IEnroll2 interface [Security]","ReuseHardwareKeyIfUnableToGenNew property","IEnroll2.ReuseHardwareKeyIfUnableToGenNew","IEnroll2.get_ReuseHardwareKeyIfUnableToGenNew","IEnroll2::ReuseHardwareKeyIfUnableToGenNew","IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew","IEnroll2::put_ReuseHardwareKeyIfUnableToGenNew","IEnroll4 interface [Security]","ReuseHardwareKeyIfUnableToGenNew property","IEnroll4.ReuseHardwareKeyIfUnableToGenNew","IEnroll4::get_ReuseHardwareKeyIfUnableToGenNew","IEnroll4::put_ReuseHardwareKeyIfUnableToGenNew","ReuseHardwareKeyIfUnableToGenNew property [Security]","ReuseHardwareKeyIfUnableToGenNew property [Security]","IEnroll2 interface","ReuseHardwareKeyIfUnableToGenNew property [Security]","IEnroll4 interface","get_ReuseHardwareKeyIfUnableToGenNew","put_ReuseHardwareKeyIfUnableToGenNew","security.ienroll4_reusehardwarekeyifunabletogennew","xenroll/IEnroll2::ReuseHardwareKeyIfUnableToGenNew","xenroll/IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew","xenroll/IEnroll2::put_ReuseHardwareKeyIfUnableToGenNew","xenroll/IEnroll4::ReuseHardwareKeyIfUnableToGenNew","xenroll/IEnroll4::get_ReuseHardwareKeyIfUnableToGenNew","xenroll/IEnroll4::put_ReuseHardwareKeyIfUnableToGenNew"]
old-location: security\ienroll4_reusehardwarekeyifunabletogennew.htm
tech.root: security
ms.assetid: d67d47f2-9d89-44ba-a5de-e1ae2bc85673
ms.date: 12/05/2018
ms.keywords: IEnroll2 interface [Security],ReuseHardwareKeyIfUnableToGenNew property, IEnroll2.ReuseHardwareKeyIfUnableToGenNew, IEnroll2.get_ReuseHardwareKeyIfUnableToGenNew, IEnroll2::ReuseHardwareKeyIfUnableToGenNew, IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew, IEnroll2::put_ReuseHardwareKeyIfUnableToGenNew, IEnroll4 interface [Security],ReuseHardwareKeyIfUnableToGenNew property, IEnroll4.ReuseHardwareKeyIfUnableToGenNew, IEnroll4::get_ReuseHardwareKeyIfUnableToGenNew, IEnroll4::put_ReuseHardwareKeyIfUnableToGenNew, ReuseHardwareKeyIfUnableToGenNew property [Security], ReuseHardwareKeyIfUnableToGenNew property [Security],IEnroll2 interface, ReuseHardwareKeyIfUnableToGenNew property [Security],IEnroll4 interface, get_ReuseHardwareKeyIfUnableToGenNew, put_ReuseHardwareKeyIfUnableToGenNew, security.ienroll4_reusehardwarekeyifunabletogennew, xenroll/IEnroll2::ReuseHardwareKeyIfUnableToGenNew, xenroll/IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew, xenroll/IEnroll2::put_ReuseHardwareKeyIfUnableToGenNew, xenroll/IEnroll4::ReuseHardwareKeyIfUnableToGenNew, xenroll/IEnroll4::get_ReuseHardwareKeyIfUnableToGenNew, xenroll/IEnroll4::put_ReuseHardwareKeyIfUnableToGenNew
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
 - IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew
 - xenroll/IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew
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
 - IEnroll2.ReuseHardwareKeyIfUnableToGenNew
 - IEnroll2.get_ReuseHardwareKeyIfUnableToGenNew
 - IEnroll2.put_ReuseHardwareKeyIfUnableToGenNew
 - IEnroll4.ReuseHardwareKeyIfUnableToGenNew
 - IEnroll4.get_ReuseHardwareKeyIfUnableToGenNew
 - IEnroll4.put_ReuseHardwareKeyIfUnableToGenNew
---

# IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ReuseHardwareKeyIfUnableToGenNew</b> property sets or retrieves a Boolean value that determines the action taken by the 
certificate enrollment control object if an error is encountered when generating a new key.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

This property is read/write.

## -parameters

## -remarks

This property is a Boolean value. This property affects only <a href="/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> (CSP) that return NTE_TOKEN_KEYSET_STORAGE_FULL. These CSPs are typically hardware-based; an example is a smart card. If this property is <b>TRUE</b> and an error is encountered while generating a new key, the certificate enrollment control object will reuse the existing hardware key. If this property is <b>FALSE</b> and an error is encountered while generating a new key, the certificate enrollment control object will not reuse the existing hardware key but will instead pass an error to the caller.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>
