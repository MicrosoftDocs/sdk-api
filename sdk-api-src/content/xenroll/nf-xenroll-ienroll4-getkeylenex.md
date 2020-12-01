---
UID: NF:xenroll.IEnroll4.GetKeyLenEx
title: IEnroll4::GetKeyLenEx (xenroll.h)
description: Retrieves size information for the signature and exchange keys.
helpviewer_keywords: ["GetKeyLenEx","GetKeyLenEx method [Security]","GetKeyLenEx method [Security]","IEnroll4 interface","IEnroll4 interface [Security]","GetKeyLenEx method","IEnroll4.GetKeyLenEx","IEnroll4::GetKeyLenEx","XEKL_KEYSIZE_INC","XEKL_KEYSIZE_MAX","XEKL_KEYSIZE_MIN","XEKL_KEYSPEC_KEYX","XEKL_KEYSPEC_SIG","security.ienroll4_getkeylenex","xenroll/IEnroll4::GetKeyLenEx"]
old-location: security\ienroll4_getkeylenex.htm
tech.root: security
ms.assetid: 377fed60-7c04-41c1-bc3d-6567d7d8c389
ms.date: 12/05/2018
ms.keywords: GetKeyLenEx, GetKeyLenEx method [Security], GetKeyLenEx method [Security],IEnroll4 interface, IEnroll4 interface [Security],GetKeyLenEx method, IEnroll4.GetKeyLenEx, IEnroll4::GetKeyLenEx, XEKL_KEYSIZE_INC, XEKL_KEYSIZE_MAX, XEKL_KEYSIZE_MIN, XEKL_KEYSPEC_KEYX, XEKL_KEYSPEC_SIG, security.ienroll4_getkeylenex, xenroll/IEnroll4::GetKeyLenEx
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
 - IEnroll4::GetKeyLenEx
 - xenroll/IEnroll4::GetKeyLenEx
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
 - IEnroll4.GetKeyLenEx
---

# IEnroll4::GetKeyLenEx


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetKeyLenEx</b> method retrieves size information for the <a href="/windows/desktop/SecGloss/s-gly">signature</a> and <a href="/windows/desktop/SecGloss/e-gly">exchange keys</a>. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

The values retrieved by this method are dependent upon the current <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a>.

## -parameters

### -param lSizeSpec [in]

Value indicating the type of size information to be retrieved. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSIZE_MIN"></a><a id="xekl_keysize_min"></a><dl>
<dt><b>XEKL_KEYSIZE_MIN</b></dt>
</dl>
</td>
<td width="60%">
Minimum key size.

</td>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSIZE_MAX"></a><a id="xekl_keysize_max"></a><dl>
<dt><b>XEKL_KEYSIZE_MAX</b></dt>
</dl>
</td>
<td width="60%">
Maximum key size.

</td>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSIZE_INC"></a><a id="xekl_keysize_inc"></a><dl>
<dt><b>XEKL_KEYSIZE_INC</b></dt>
</dl>
</td>
<td width="60%">
Size of key increment. For more information, see Remarks.

</td>
</tr>
</table>

### -param lKeySpec [in]

Specifies the key for which size information is returned. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSPEC_KEYX"></a><a id="xekl_keyspec_keyx"></a><dl>
<dt><b>XEKL_KEYSPEC_KEYX</b></dt>
</dl>
</td>
<td width="60%">
Exchange key

</td>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSPEC_SIG"></a><a id="xekl_keyspec_sig"></a><dl>
<dt><b>XEKL_KEYSPEC_SIG</b></dt>
</dl>
</td>
<td width="60%">
Signature key

</td>
</tr>
</table>

### -param pdwKeySize [out]

A pointer to <b>LONG</b> that receives the key size information, in bits.

## -remarks

If the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> does not support this method, an error is returned.

For additional details on the XEKL_KEYSIZE_INC value, see PP_SIG_KEYSIZE_INC usage in the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a> reference page.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>