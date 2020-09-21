---
UID: NF:xenroll.IEnroll4.binaryBlobToString
title: IEnroll4::binaryBlobToString (xenroll.h)
description: Converts a binary data BLOB to a string. This method uses the CryptBinaryToString function to perform the conversion. This method was first defined in the IEnroll4 interface.
helpviewer_keywords: ["IEnroll4 interface [Security]","binaryBlobToString method","IEnroll4.binaryBlobToString","IEnroll4::binaryBlobToString","binaryBlobToString","binaryBlobToString method [Security]","binaryBlobToString method [Security]","IEnroll4 interface","security.ienroll4_binaryblobtostring","xenroll/IEnroll4::binaryBlobToString"]
old-location: security\ienroll4_binaryblobtostring.htm
tech.root: security
ms.assetid: 0ce10b31-29f4-4fda-a488-7bc124e9461e
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],binaryBlobToString method, IEnroll4.binaryBlobToString, IEnroll4::binaryBlobToString, binaryBlobToString, binaryBlobToString method [Security], binaryBlobToString method [Security],IEnroll4 interface, security.ienroll4_binaryblobtostring, xenroll/IEnroll4::binaryBlobToString
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
 - IEnroll4::binaryBlobToString
 - xenroll/IEnroll4::binaryBlobToString
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
 - IEnroll4.binaryBlobToString
---

# IEnroll4::binaryBlobToString


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>binaryBlobToString</b> method converts a binary data <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> to a string. This method uses the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptbinarytostringa">CryptBinaryToString</a> function to perform the conversion. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param Flags [in]

Value passed to the <i>dwFlags</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptbinarytostringa">CryptBinaryToString</a> function. For a description of possible values, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptbinarytostringa">CryptBinaryToString</a>.

### -param pblobBinary [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> that represents the binary BLOB to  convert to a string.

### -param ppwszString [out]

A pointer to a <b>LPWSTR</b> that receives the encoded data.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>