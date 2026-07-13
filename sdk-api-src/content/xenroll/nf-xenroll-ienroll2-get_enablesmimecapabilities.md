---
UID: NF:xenroll.IEnroll2.get_EnableSMIMECapabilities
title: IEnroll2::get_EnableSMIMECapabilities (xenroll.h)
description: Controls whether the PKCS (Get)
helpviewer_keywords: ["EnableSMIMECapabilities property [Security]","EnableSMIMECapabilities property [Security]","IEnroll2 interface","IEnroll2 interface [Security]","EnableSMIMECapabilities property","IEnroll2.EnableSMIMECapabilities","IEnroll2.get_EnableSMIMECapabilities","IEnroll2::EnableSMIMECapabilities","IEnroll2::get_EnableSMIMECapabilities","IEnroll2::put_EnableSMIMECapabilities","get_EnableSMIMECapabilities","security.ienroll4_enablesmimecapabilities","xenroll/IEnroll2::EnableSMIMECapabilities","xenroll/IEnroll2::get_EnableSMIMECapabilities","xenroll/IEnroll2::put_EnableSMIMECapabilities"]
old-location: security\ienroll4_enablesmimecapabilities.htm
tech.root: security
ms.assetid: e0571a8c-c682-44fd-a479-ace627b314b5
ms.date: 12/05/2018
ms.keywords: EnableSMIMECapabilities property [Security], EnableSMIMECapabilities property [Security],IEnroll2 interface, IEnroll2 interface [Security],EnableSMIMECapabilities property, IEnroll2.EnableSMIMECapabilities, IEnroll2.get_EnableSMIMECapabilities, IEnroll2::EnableSMIMECapabilities, IEnroll2::get_EnableSMIMECapabilities, IEnroll2::put_EnableSMIMECapabilities, get_EnableSMIMECapabilities, security.ienroll4_enablesmimecapabilities, xenroll/IEnroll2::EnableSMIMECapabilities, xenroll/IEnroll2::get_EnableSMIMECapabilities, xenroll/IEnroll2::put_EnableSMIMECapabilities
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
 - IEnroll2::get_EnableSMIMECapabilities
 - xenroll/IEnroll2::get_EnableSMIMECapabilities
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
 - IEnroll2.EnableSMIMECapabilities
 - IEnroll2.get_EnableSMIMECapabilities
 - IEnroll2.put_EnableSMIMECapabilities
---

# IEnroll2::get_EnableSMIMECapabilities


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>EnableSMIMECapabilities</b> property controls whether the PKCS #10 will contain a signed attribute for <a href="/windows/desktop/SecGloss/s-gly">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) capabilities.

The default value for this property is <b>FALSE</b>. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll2</a>
