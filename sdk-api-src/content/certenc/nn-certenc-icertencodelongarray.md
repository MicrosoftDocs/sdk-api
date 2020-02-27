---
UID: NN:certenc.ICertEncodeLongArray
title: ICertEncodeLongArray (certenc.h)
description: Provides methods for handling Long arrays used in certificate extensions.
old-location: security\icertencodelongarray.htm
tech.root: SecCrypto
ms.assetid: e8555282-6c09-4f23-830e-358bc73287ee
ms.date: 12/05/2018
ms.keywords: ICertEncodeLongArray, ICertEncodeLongArray interface [Security], ICertEncodeLongArray interface [Security],described, _certsrv_icertencodelongarray, certenc/ICertEncodeLongArray, security.icertencodelongarray
f1_keywords:
- certenc/ICertEncodeLongArray
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Certenc.dll
api_name:
- ICertEncodeLongArray
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertEncodeLongArray interface


## -description


The <b>ICertEncodeLongArray</b> interface provides methods for handling <b>Long</b> arrays used in certificate extensions.

 A certificate extension can be created by using a <b>Long</b> array stored in an 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/writing-custom-extension-handlers">extension handler</a> COM object instantiated by the policy module. Each element in the array is a <b>Long</b> value.

This interface is provided mainly as a demonstration for encoding custom extensions. The Certificate Services sample programs in the Platform Software Development Kit (SDK) contain source code for this interface.

<b>ICertEncodeLongArray</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeLongArray</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform SDK.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertEncodeLongArray</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertEncodeLongArray</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertEncodeLongArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-decode">Decode</a>
</td>
<td align="left" width="63%">
Decodes an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded <b>Long</b> array and stores the resulting array of <b>Long</b> in the COM object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-encode">Encode</a>
</td>
<td align="left" width="63%">
Performs ASN.1 encoding on a <b>Long</b> array stored in the COM object and returns the ASN.1-encoded <b>Long</b> array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of <b>Long</b> values in a <b>Long</b> array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Returns the <b>Long</b> value at a specified index of a <b>Long</b> array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets a <b>Long</b> array to a specified number of elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-setvalue">SetValue</a>
</td>
<td align="left" width="63%">
Sets a <b>Long</b> value at a specified index of a <b>Long</b> array.

</td>
</tr>
</table> 

