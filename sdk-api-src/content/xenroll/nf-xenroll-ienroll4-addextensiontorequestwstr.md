---
UID: NF:xenroll.IEnroll4.addExtensionToRequestWStr
title: IEnroll4::addExtensionToRequestWStr (xenroll.h)
description: Adds an extension to the request.
helpviewer_keywords: ["IEnroll4 interface [Security]","addExtensionToRequestWStr method","IEnroll4.addExtensionToRequestWStr","IEnroll4::addExtensionToRequestWStr","addExtensionToRequestWStr","addExtensionToRequestWStr method [Security]","addExtensionToRequestWStr method [Security]","IEnroll4 interface","security.ienroll4_addextensiontorequestwstr","xenroll/IEnroll4::addExtensionToRequestWStr"]
old-location: security\ienroll4_addextensiontorequestwstr.htm
tech.root: security
ms.assetid: 4ecca64b-a8f4-4816-8bf1-7b8e74262ac0
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],addExtensionToRequestWStr method, IEnroll4.addExtensionToRequestWStr, IEnroll4::addExtensionToRequestWStr, addExtensionToRequestWStr, addExtensionToRequestWStr method [Security], addExtensionToRequestWStr method [Security],IEnroll4 interface, security.ienroll4_addextensiontorequestwstr, xenroll/IEnroll4::addExtensionToRequestWStr
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
 - IEnroll4::addExtensionToRequestWStr
 - xenroll/IEnroll4::addExtensionToRequestWStr
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
 - IEnroll4.addExtensionToRequestWStr
---

# IEnroll4::addExtensionToRequestWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addExtensionToRequestWStr</b> method adds an extension to the request. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param Flags [in]

Specifies whether the extension is critical. 
If <b>TRUE</b>, the extension being added is critical. If <b>FALSE</b>, it is not critical.

### -param pwszName [in]

A pointer to a null-terminated wide character string that represents the Object Identifier (OID) for the extension name.

### -param pblobValue [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that represents the extension value.

## -returns

The return value is an <b>HRESULT</b>, with S_OK returned if the call is successful.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>