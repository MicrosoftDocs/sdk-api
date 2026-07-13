---
UID: NF:certenroll.IAlternativeName.InitializeFromOtherName
title: IAlternativeName::InitializeFromOtherName (certenroll.h)
description: Initializes the object from an object identifier (OID) and the associated raw data (byte array).
helpviewer_keywords: ["IAlternativeName interface [Security]","InitializeFromOtherName method","IAlternativeName.InitializeFromOtherName","IAlternativeName::InitializeFromOtherName","InitializeFromOtherName","InitializeFromOtherName method [Security]","InitializeFromOtherName method [Security]","IAlternativeName interface","certenroll/IAlternativeName::InitializeFromOtherName","security.ialternativename_initializefromothername_method"]
old-location: security\ialternativename_initializefromothername_method.htm
tech.root: security
ms.assetid: cd697085-0e8e-4a18-a7c5-77cd4927f664
ms.date: 12/05/2018
ms.keywords: IAlternativeName interface [Security],InitializeFromOtherName method, IAlternativeName.InitializeFromOtherName, IAlternativeName::InitializeFromOtherName, InitializeFromOtherName, InitializeFromOtherName method [Security], InitializeFromOtherName method [Security],IAlternativeName interface, certenroll/IAlternativeName::InitializeFromOtherName, security.ialternativename_initializefromothername_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAlternativeName::InitializeFromOtherName
 - certenroll/IAlternativeName::InitializeFromOtherName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IAlternativeName.InitializeFromOtherName
---

# IAlternativeName::InitializeFromOtherName


## -description

The <b>InitializeFromOtherName</b> method initializes the object from an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and the associated raw data (byte array). This method is provided to support the <b>otherName</b> field in the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) <b>AlternativeNames</b> extension declaration.

``` syntax

----------------------------------------------------------------------
-- AlternativeNames 
-- XCN_OID_SUBJECT_ALT_NAME2 (2.5.29.17)
----------------------------------------------------------------------

AltNames ::= SEQUENCE --#public-- OF GeneralName
GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5STRING,
   dNSName                 [2] IMPLICIT IA5STRING,
   x400Address             [3] IMPLICIT SeqOfAny,       -- Not supported
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SeqOfAny,
   uniformResourceLocator  [6] IMPLICIT IA5STRING,
   iPAddress               [7] IMPLICIT OCTETSTRING,
   registeredID            [8] IMPLICIT EncodedObjectID -- Not supported
}

OtherName ::= SEQUENCE 
{
   type                    EncodedObjectID,
   value                   [0] EXPLICIT NOCOPYANY 
}

```


## -parameters

### -param pObjectId [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that represents an OID.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that identifies the type of Unicode encoding applied to the <i>strRawData</i> parameter.

### -param strRawData [in]

A <b>BSTR</b> variable that contains the name associated with the OID.

### -param ToBeWrapped [in]

A <b>VARIANT_BOOL</b> variable that identifies whether the input string contained in the <i>strRawData</i> parameter is encoded and saved as an octet string (byte array).

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>

## -remarks

You can use this function to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a> object from an OID and an associated string value. The string is Unicode encoded. If you specify true for the <i>ToBeWrapped</i> parameter, the string is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER). You can retrieve the OID by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-get_objectid">ObjectId</a> property. You can retrieve the encoded string or, if <i>ToBeWrapped</i> is true, the DER-encoded byte array by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-get_rawdata">RawData</a> property to retrieve the encoded byte array.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>
