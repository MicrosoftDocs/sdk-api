---
UID: NF:xenroll.IEnroll.enumContainersWStr
title: IEnroll::enumContainersWStr (xenroll.h)
description: Retrieves the names of containers for the cryptographic service provider (CSP) specified by the ProviderNameWStr property.
helpviewer_keywords: ["IEnroll interface [Security]","enumContainersWStr method","IEnroll.enumContainersWStr","IEnroll::enumContainersWStr","enumContainersWStr","enumContainersWStr method [Security]","enumContainersWStr method [Security]","IEnroll interface","security.ienroll4_enumcontainerswstr","xenroll/IEnroll::enumContainersWStr"]
old-location: security\ienroll4_enumcontainerswstr.htm
tech.root: security
ms.assetid: a08d97c9-8ee9-464e-862e-18c335695927
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],enumContainersWStr method, IEnroll.enumContainersWStr, IEnroll::enumContainersWStr, enumContainersWStr, enumContainersWStr method [Security], enumContainersWStr method [Security],IEnroll interface, security.ienroll4_enumcontainerswstr, xenroll/IEnroll::enumContainersWStr
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
 - IEnroll::enumContainersWStr
 - xenroll/IEnroll::enumContainersWStr
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
 - IEnroll.enumContainersWStr
---

# IEnroll::enumContainersWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>enumContainersWStr</b> method retrieves the names of containers for the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) specified by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr">ProviderNameWStr</a> property. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

## -parameters

### -param dwIndex [in]

Specifies the ordinal position of the container whose name will be retrieved. Specify zero for the first container.

### -param pbstr [out]

A pointer to a <b>LPWSTR</b> variable that receives the name of the container.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. The value ERROR_NO_MORE_ITEMS is returned when there are no more items.

## -remarks

If the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr">ProviderNameWStr</a> property value has not been set, the default value (usually Microsoft Base Cryptographic Provider) of <b>ProviderNameWStr</b> as set in the registry is used.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>