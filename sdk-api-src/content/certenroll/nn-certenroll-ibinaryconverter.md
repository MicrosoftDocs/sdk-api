---
UID: NN:certenroll.IBinaryConverter
title: IBinaryConverter (certenroll.h)
description: Contains general methods that enable you to create a Unicode-encoded string from a byte array, create a byte array from a Unicode-encoded string, and modify the type of Unicode encoding applied to a string.
old-location: security\ibinaryconverter.htm
tech.root: seccertenroll
ms.assetid: 495a321a-3005-4537-b082-5003e437d21f
ms.date: 12/05/2018
ms.keywords: IBinaryConverter, IBinaryConverter interface [Security], IBinaryConverter interface [Security],described, certenroll/IBinaryConverter, security.ibinaryconverter
ms.topic: interface
f1_keywords:
- certenroll/IBinaryConverter
dev_langs:
- c++
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CertEnroll.dll
api_name:
- IBinaryConverter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBinaryConverter interface


## -description


The <b>IBinaryConverter</b> interface contains general methods that enable you to create a Unicode-encoded string from a byte array, create a byte array from a Unicode-encoded string, and modify the type of Unicode encoding applied to  a string. You can use this interface to represent a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate BLOB</a> as a printable string or to decode the string back into a certificate BLOB.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBinaryConverter</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IBinaryConverter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBinaryConverter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ibinaryconverter-stringtostring">StringToString</a>
</td>
<td align="left" width="63%">
Modifies the type of Unicode encoding applied to a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray">StringToVariantByteArray</a>
</td>
<td align="left" width="63%">
Creates a byte array from a Unicode encoded string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ibinaryconverter-variantbytearraytostring">VariantByteArrayToString</a>
</td>
<td align="left" width="63%">
Creates a Unicode encoded string from a byte array.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

