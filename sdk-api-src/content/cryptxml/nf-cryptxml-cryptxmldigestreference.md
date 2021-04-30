---
UID: NF:cryptxml.CryptXmlDigestReference
title: CryptXmlDigestReference function (cryptxml.h)
description: Is used by an application to digest the resolved reference. This function applies transforms before updating the digest.
helpviewer_keywords: ["CRYPT_XML_REFERENCE_DATA_TRANSFORMED","CryptXmlDigestReference","CryptXmlDigestReference function [Security]","cryptxml/CryptXmlDigestReference","security.cryptxmldigestreference"]
old-location: security\cryptxmldigestreference.htm
tech.root: security
ms.assetid: 781bacc2-6783-4884-8290-a36f917c17c1
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_REFERENCE_DATA_TRANSFORMED, CryptXmlDigestReference, CryptXmlDigestReference function [Security], cryptxml/CryptXmlDigestReference, security.cryptxmldigestreference
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptXmlDigestReference
 - cryptxml/CryptXmlDigestReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlDigestReference
---

# CryptXmlDigestReference function


## -description

The <b>CryptXmlDigestReference</b> function is used by an application to digest the resolved reference. This function applies transforms before updating the digest.

## -parameters

### -param hReference [in]

The  handle of a <b>Reference</b> element.

### -param dwFlags

Specifies values that control how the process applies transforms.


Currently defined <i>dwFlags</i> are shown in the following table.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_REFERENCE_DATA_TRANSFORMED"></a><a id="crypt_xml_reference_data_transformed"></a><dl>
<dt><b>CRYPT_XML_REFERENCE_DATA_TRANSFORMED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Specifies that the processing engine will create the digest without applying the transform chain engine.

</td>
</tr>
</table>

### -param pDataProviderIn [in]

A pointer to a    <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_data_provider">CRYPT_XML_DATA_PROVIDER</a> structure that specifies the data provider. The <b>CryptXmlDigestReference</b> function always calls the <b>fpnClose</b> function on the data provider.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.

## -remarks

    When the <b>CRYPT_XML_REFERENCE_DATA_TRANSFORMED</b> flag is set,
    the processing engine adds received data directly to the digest without 
    applying the transform chain engine.

<div class="alert"><b>Note</b>  The <b>CryptXmlDigestReference</b> function always calls the function pointed to by the <b>fpnClose</b> member of the <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_data_provider">CRYPT_XML_DATA_PROVIDER</a> structure pointed to by the <i>pDataProviderIn</i> parameter.
</div>
<div> </div>