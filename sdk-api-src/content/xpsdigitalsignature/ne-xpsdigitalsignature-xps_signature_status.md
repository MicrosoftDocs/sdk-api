---
UID: NE:xpsdigitalsignature.__MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0001
title: XPS_SIGNATURE_STATUS (xpsdigitalsignature.h)
description: Describes the status of a document's digital signature.
helpviewer_keywords: ["XPS_SIGNATURE_STATUS","XPS_SIGNATURE_STATUS enumeration [XPS Documents and Packaging]","XPS_SIGNATURE_STATUS_BROKEN","XPS_SIGNATURE_STATUS_INCOMPLETE","XPS_SIGNATURE_STATUS_INCOMPLIANT","XPS_SIGNATURE_STATUS_QUESTIONABLE","XPS_SIGNATURE_STATUS_VALID","xps.xps_signature_status","xpsdigitalsignature/XPS_SIGNATURE_STATUS","xpsdigitalsignature/XPS_SIGNATURE_STATUS_BROKEN","xpsdigitalsignature/XPS_SIGNATURE_STATUS_INCOMPLETE","xpsdigitalsignature/XPS_SIGNATURE_STATUS_INCOMPLIANT","xpsdigitalsignature/XPS_SIGNATURE_STATUS_QUESTIONABLE","xpsdigitalsignature/XPS_SIGNATURE_STATUS_VALID"]
old-location: xps\xps_signature_status.htm
tech.root: xps
ms.assetid: 8c03749c-49cf-4d9c-90be-a75412f044ec
ms.date: 12/05/2018
ms.keywords: XPS_SIGNATURE_STATUS, XPS_SIGNATURE_STATUS enumeration [XPS Documents and Packaging], XPS_SIGNATURE_STATUS_BROKEN, XPS_SIGNATURE_STATUS_INCOMPLETE, XPS_SIGNATURE_STATUS_INCOMPLIANT, XPS_SIGNATURE_STATUS_QUESTIONABLE, XPS_SIGNATURE_STATUS_VALID, xps.xps_signature_status, xpsdigitalsignature/XPS_SIGNATURE_STATUS, xpsdigitalsignature/XPS_SIGNATURE_STATUS_BROKEN, xpsdigitalsignature/XPS_SIGNATURE_STATUS_INCOMPLETE, xpsdigitalsignature/XPS_SIGNATURE_STATUS_INCOMPLIANT, xpsdigitalsignature/XPS_SIGNATURE_STATUS_QUESTIONABLE, xpsdigitalsignature/XPS_SIGNATURE_STATUS_VALID
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XPS_SIGNATURE_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0001
 - xpsdigitalsignature/__MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0001
 - XPS_SIGNATURE_STATUS
 - xpsdigitalsignature/XPS_SIGNATURE_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsdigitalsignature.h
api_name:
 - XPS_SIGNATURE_STATUS
---

# XPS_SIGNATURE_STATUS enumeration


## -description

Describes the status of a document's digital signature.

## -enum-fields

### -field XPS_SIGNATURE_STATUS_INCOMPLIANT:1

The signature violates one or more  signing rules stated in section 10.2.1.2 of the   <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>. These rules describe the parts or relationships that must or must not be signed.

A signature that is incompliant must be created as such. 
Changing signed content cannot make a valid signature incompliant. One example of an incompliant signature  is the signature of a   package that has an unknown relationships type at the root.

### -field XPS_SIGNATURE_STATUS_INCOMPLETE:2

The signature does not include parts that must be signed.

If a valid XPS signature is created and the XPS document contents are later modified, the signature will become incomplete or broken.
For example, removing a page from a FixedDocument makes the signature incomplete; it also breaks the signature,  but  the fact that the signature is incomplete is of greater importance.

### -field XPS_SIGNATURE_STATUS_BROKEN:3

This is a compliant digital signature, but it fails the signature validation routines described in the <i>Open Packaging Conventions</i> (refer to See Also).

Modification of the markup in a FixedPage that has been signed breaks the signature.

### -field XPS_SIGNATURE_STATUS_QUESTIONABLE:4

This is not an incompliant or broken digital signature, but the signed content (parts and relationships) includes elements or attributes from an unknown namespace introduced through the markup compatibility mechanisms.

### -field XPS_SIGNATURE_STATUS_VALID:5

This is a valid signature: it is not broken, incompliant, or questionable. The application, however,  must still check the certificate trust chain, revocation lists, and expiration dates.

## -remarks

The digital signature status values correspond to section 10.2.1.2 in the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>.

The Open Packaging Conventions are specified in   the 1st edition, Part 2, "Open Packaging Conventions," of <a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">Standard ECMA-376, Office Open XML File Formats</a>.

<div class="alert"><b>Note</b>  These resources may not be available in some languages 

and countries.</div>
<div> </div>

## -see-also

<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>

