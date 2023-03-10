---
UID: NF:certenc.ICertEncodeAltName.Reset
title: ICertEncodeAltName::Reset (certenc.h)
description: Specifies the size of the alternate name array in this object. The value of all elements in the array are set to zero.
helpviewer_keywords: ["CCertEncodeAltName object [Security]","Reset method","ICertEncodeAltName interface [Security]","Reset method","ICertEncodeAltName.Reset","ICertEncodeAltName::Reset","Reset","Reset method [Security]","Reset method [Security]","CCertEncodeAltName object","Reset method [Security]","ICertEncodeAltName interface","certenc/ICertEncodeAltName::Reset","security.icertencodealtname_reset"]
old-location: security\icertencodealtname_reset.htm
tech.root: security
ms.assetid: 99aa43fe-534b-4696-8bfc-7049b16be1cf
ms.date: 12/05/2018
ms.keywords: CCertEncodeAltName object [Security],Reset method, ICertEncodeAltName interface [Security],Reset method, ICertEncodeAltName.Reset, ICertEncodeAltName::Reset, Reset, Reset method [Security], Reset method [Security],CCertEncodeAltName object, Reset method [Security],ICertEncodeAltName interface, certenc/ICertEncodeAltName::Reset, security.icertencodealtname_reset
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertEncodeAltName::Reset
 - certenc/ICertEncodeAltName::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeAltName.Reset
 - CCertEncodeAltName.Reset
---

# ICertEncodeAltName::Reset


## -description

The <b>Reset</b> method specifies the size of the alternate name array in this object. The value of all elements in the array are set to zero.

## -parameters

### -param NameCount [in]

Specifies the number of elements in the array.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodealtname">ICertEncodeAltName</a>