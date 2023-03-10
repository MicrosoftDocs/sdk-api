---
UID: NF:cryptxml.CryptXmlGetAlgorithmInfo
title: CryptXmlGetAlgorithmInfo function (cryptxml.h)
description: Decodes the CRYPT_XML_ALGORITHM structure and returns information about the algorithm.
helpviewer_keywords: ["CRYPT_XML_FLAG_DISABLE_EXTENSIONS","CryptXmlGetAlgorithmInfo","CryptXmlGetAlgorithmInfo function [Security]","cryptxml/CryptXmlGetAlgorithmInfo","security.cryptxmlgetalgorithminfo"]
old-location: security\cryptxmlgetalgorithminfo.htm
tech.root: security
ms.assetid: 6def15be-d88f-4e2b-b579-eea7742d77b0
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_FLAG_DISABLE_EXTENSIONS, CryptXmlGetAlgorithmInfo, CryptXmlGetAlgorithmInfo function [Security], cryptxml/CryptXmlGetAlgorithmInfo, security.cryptxmlgetalgorithminfo
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
 - CryptXmlGetAlgorithmInfo
 - cryptxml/CryptXmlGetAlgorithmInfo
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
 - CryptXmlGetAlgorithmInfo
---

# CryptXmlGetAlgorithmInfo function


## -description

The <b>CryptXmlGetAlgorithmInfo</b> function decodes the <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm">CRYPT_XML_ALGORITHM</a> structure and returns information about the algorithm.

## -parameters

### -param pXmlAlgorithm [in]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm">CRYPT_XML_ALGORITHM</a> structure that specifies the algorithm about which to return information.

### -param dwFlags

This parameter can be one of the following values.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_FLAG_DISABLE_EXTENSIONS"></a><a id="crypt_xml_flag_disable_extensions"></a><dl>
<dt><b>CRYPT_XML_FLAG_DISABLE_EXTENSIONS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Only default implementations for the signature and
digest  are used.  When this flag is set, no other registered extensions are loaded.

</td>
</tr>
</table>

### -param ppAlgInfo [out]

A pointer to a pointer to a  <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm_info">CRYPT_XML_ALGORITHM_INFO</a> structure. When you have finished using the memory pointed to by the <i>ppAlgInfo</i> parameter, free it by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.