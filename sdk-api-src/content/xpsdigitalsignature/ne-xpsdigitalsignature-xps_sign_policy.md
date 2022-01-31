---
UID: NE:xpsdigitalsignature.__MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0002
title: XPS_SIGN_POLICY (xpsdigitalsignature.h)
description: A bitwise enumerator that indicates which, if any, optional parts of an XPS document are signed.
helpviewer_keywords: ["XPS_SIGN_POLICY","XPS_SIGN_POLICY enumeration [XPS Documents and Packaging]","XPS_SIGN_POLICY_ALL","XPS_SIGN_POLICY_CORE_PROPERTIES","XPS_SIGN_POLICY_DISCARD_CONTROL","XPS_SIGN_POLICY_NONE","XPS_SIGN_POLICY_PRINT_TICKET","XPS_SIGN_POLICY_SIGNATURE_RELATIONSHIPS","xps.xps_sign_policy","xpsdigitalsignature/XPS_SIGN_POLICY","xpsdigitalsignature/XPS_SIGN_POLICY_ALL","xpsdigitalsignature/XPS_SIGN_POLICY_CORE_PROPERTIES","xpsdigitalsignature/XPS_SIGN_POLICY_DISCARD_CONTROL","xpsdigitalsignature/XPS_SIGN_POLICY_NONE","xpsdigitalsignature/XPS_SIGN_POLICY_PRINT_TICKET","xpsdigitalsignature/XPS_SIGN_POLICY_SIGNATURE_RELATIONSHIPS"]
old-location: xps\xps_sign_policy.htm
tech.root: xps
ms.assetid: 88191931-4d6f-4ef3-ba75-227f6d2c2b10
ms.date: 12/05/2018
ms.keywords: XPS_SIGN_POLICY, XPS_SIGN_POLICY enumeration [XPS Documents and Packaging], XPS_SIGN_POLICY_ALL, XPS_SIGN_POLICY_CORE_PROPERTIES, XPS_SIGN_POLICY_DISCARD_CONTROL, XPS_SIGN_POLICY_NONE, XPS_SIGN_POLICY_PRINT_TICKET, XPS_SIGN_POLICY_SIGNATURE_RELATIONSHIPS, xps.xps_sign_policy, xpsdigitalsignature/XPS_SIGN_POLICY, xpsdigitalsignature/XPS_SIGN_POLICY_ALL, xpsdigitalsignature/XPS_SIGN_POLICY_CORE_PROPERTIES, xpsdigitalsignature/XPS_SIGN_POLICY_DISCARD_CONTROL, xpsdigitalsignature/XPS_SIGN_POLICY_NONE, xpsdigitalsignature/XPS_SIGN_POLICY_PRINT_TICKET, xpsdigitalsignature/XPS_SIGN_POLICY_SIGNATURE_RELATIONSHIPS
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
req.typenames: XPS_SIGN_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0002
 - xpsdigitalsignature/__MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0002
 - XPS_SIGN_POLICY
 - xpsdigitalsignature/XPS_SIGN_POLICY
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
 - XPS_SIGN_POLICY
---

# XPS_SIGN_POLICY enumeration


## -description

A bitwise enumerator that indicates which, if any, optional parts of an XPS document are signed.

## -enum-fields

### -field XPS_SIGN_POLICY_NONE:0

No optional parts or relationships are signed.

### -field XPS_SIGN_POLICY_CORE_PROPERTIES:0x1

The CoreProperties part and the relationships that include it are signed.

### -field XPS_SIGN_POLICY_SIGNATURE_RELATIONSHIPS:0x2

The signature relationships  from the signature origin part are signed. <i>Signature relationships</i> are those relationships that have a <i>digital signature</i> relationship type.

<div class="alert"><b>Note</b>  <p class="note">Setting the <b>XPS_SIGN_POLICY_SIGNATURE_RELATIONSHIPS</b> flag will cause the signature relationships that start from the signature origin part to be signed. Signatures that are made with this flag set will break when new signatures are added later, because new  signatures  add new signature relationships.

</div>
<div> </div>

### -field XPS_SIGN_POLICY_PRINT_TICKET:0x4

The  PrintTicket part and the relationships that include it are signed.

### -field XPS_SIGN_POLICY_DISCARD_CONTROL:0x8

The  DiscardControl part and the relationships that include it are signed.

### -field XPS_SIGN_POLICY_ALL:0xf

The  CoreProperties part and the relationships that include it, the digital signature relationship type from the SignatureOrigin part, the PrintTicket part and the relationships that include it, and the DiscardControl part and the relationships that include it are all signed.

<div class="alert"><b>Note</b>  <p class="note">Setting the <b>XPS_SIGN_POLICY_ALL</b> sets the <b>XPS_SIGN_POLICY_SIGNATURE_RELATIONSHIPS</b> flag, which will cause the signature relationships that start from the signature origin part to be signed. Signatures that are made with this flag set will break when new signatures are added later, because new  signatures  add new signature relationships.

</div>
<div> </div>

## -remarks

More than one value may be set.

## -see-also

<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>

