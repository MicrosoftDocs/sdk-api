---
UID: NF:certenroll.IAlternativeName.InitializeFromOtherName
title: IAlternativeName::InitializeFromOtherName (certenroll.h)
author: windows-sdk-content
description: Initializes the object from an object identifier (OID) and the associated raw data (byte array).
old-location: security\ialternativename_initializefromothername_method.htm
tech.root: seccertenroll
ms.assetid: cd697085-0e8e-4a18-a7c5-77cd4927f664
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAlternativeName interface [Security],InitializeFromOtherName method, IAlternativeName.InitializeFromOtherName, IAlternativeName::InitializeFromOtherName, InitializeFromOtherName, InitializeFromOtherName method [Security], InitializeFromOtherName method [Security],IAlternativeName interface, certenroll/IAlternativeName::InitializeFromOtherName, security.ialternativename_initializefromothername_method
ms.topic: method
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
 - IAlternativeName.InitializeFromOtherName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAlternativeName::InitializeFromOtherName


## -description


The <b>InitializeFromOtherName</b> method initializes the object from an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and the associated raw data (byte array). This method is provided to support the <b>otherName</b> field in the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) <b>AlternativeNames</b> extension declaration.
<pre class="syntax" xml:space="preserve"><code>
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
</code></pre>

## -parameters




### -param pObjectId [in]

Pointer to an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface that represents an OID.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that identifies the type of Unicode encoding applied to the <i>strRawData</i> parameter.


### -param strRawData [in]

A <b>BSTR</b> variable that contains the name associated with the OID.


### -param ToBeWrapped [in]

A <b>VARIANT_BOOL</b> variable that identifies whether the input string contained in the <i>strRawData</i> parameter is encoded and saved as an octet string (byte array).


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



You can use this function to initialize an <a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a> object from an OID and an associated string value. The string is Unicode encoded. If you specify true for the <i>ToBeWrapped</i> parameter, the string is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER). You can retrieve the OID by calling the <a href="https://msdn.microsoft.com/be14756b-a7dc-40f4-ae09-b576f85837f6">ObjectId</a> property. You can retrieve the encoded string or, if <i>ToBeWrapped</i> is true, the DER-encoded byte array by calling the <a href="https://msdn.microsoft.com/7385654d-03f8-4796-a95c-000fa8ab65a3">RawData</a> property to retrieve the encoded byte array.




## -see-also




<a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a>
 

 

