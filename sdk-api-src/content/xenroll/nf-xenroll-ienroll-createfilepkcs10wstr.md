---
UID: NF:xenroll.IEnroll.createFilePKCS10WStr
title: IEnroll::createFilePKCS10WStr (xenroll.h)
description: Creates a base64-encoded PKCS (IEnroll.createFilePKCS10WStr)
helpviewer_keywords: ["IEnroll interface [Security]","createFilePKCS10WStr method","IEnroll.createFilePKCS10WStr","IEnroll::createFilePKCS10WStr","createFilePKCS10WStr","createFilePKCS10WStr method [Security]","createFilePKCS10WStr method [Security]","IEnroll interface","security.ienroll4_createfilepkcs10wstr","xenroll/IEnroll::createFilePKCS10WStr"]
old-location: security\ienroll4_createfilepkcs10wstr.htm
tech.root: security
ms.assetid: 5edd54c5-9dfb-44b8-a293-4fe6a8de45e3
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],createFilePKCS10WStr method, IEnroll.createFilePKCS10WStr, IEnroll::createFilePKCS10WStr, createFilePKCS10WStr, createFilePKCS10WStr method [Security], createFilePKCS10WStr method [Security],IEnroll interface, security.ienroll4_createfilepkcs10wstr, xenroll/IEnroll::createFilePKCS10WStr
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
 - IEnroll::createFilePKCS10WStr
 - xenroll/IEnroll::createFilePKCS10WStr
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
 - IEnroll.createFilePKCS10WStr
---

# IEnroll::createFilePKCS10WStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createFilePKCS10WStr</b> method creates a base64-encoded PKCS #10 <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> and saves it in a file. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This method differs from 
the <a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a> method only in saving the base64-encoded PKCS #10 certificate request  to the file specified by the <i>wszPKCS10FileName</i> parameter.

## -parameters

### -param DNName [in]

The distinguished name (DN) of the entity for which the request is being made. <i>DNName</i> must follow the <a href="/windows/desktop/SecGloss/x-gly">X.500</a> naming convention. For example, "CN=User, O=Microsoft". If a two-letter prefix does not exist, an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) may be provided instead.

### -param Usage [in]

An <a href="/windows/desktop/SecGloss/o-gly">OID</a> that describes the purpose of the certificate being generated, for example, individual or commercial Authenticode certificate, or client authentication. You can also specify multiple OIDs separated by a comma.

The OID is passed through to the PKCS #10 request. The control does not examine the OID.

### -param wszPKCS10FileName [in]

The name of the file in which the base64-encoded PKCS #10 is saved. The contents of this file may be submitted to a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> for processing.

## -remarks

By default, the Microsoft Base Cryptographic Provider is used, and a unique signature key is created.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
