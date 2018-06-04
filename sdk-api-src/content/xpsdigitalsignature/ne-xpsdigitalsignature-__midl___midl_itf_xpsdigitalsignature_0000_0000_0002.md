---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0002 enumeration


## -description


A bitwise enumerator that indicates which, if any, optional parts of an XPS document are signed.


## -enum-fields




### -field XPS_SIGN_POLICY_NONE

No optional parts or relationships are signed.


### -field XPS_SIGN_POLICY_CORE_PROPERTIES

The CoreProperties part and the relationships that include it are signed.


### -field XPS_SIGN_POLICY_SIGNATURE_RELATIONSHIPS

The signature relationships  from the signature origin part are signed. <i>Signature relationships</i> are those relationships that have a <i>digital signature</i> relationship type.

<div class="alert"><b>Note</b>  <p class="note">Setting the <b>XPS_SIGN_POLICY_SIGNATURE_RELATIONSHIPS</b> flag will cause the signature relationships that start from the signature origin part to be signed. Signatures that are made with this flag set will break when new signatures are added later, because new  signatures  add new signature relationships.

</div>
<div> </div>

### -field XPS_SIGN_POLICY_PRINT_TICKET

The  PrintTicket part and the relationships that include it are signed.


### -field XPS_SIGN_POLICY_DISCARD_CONTROL

The  DiscardControl part and the relationships that include it are signed.


### -field XPS_SIGN_POLICY_ALL

The  CoreProperties part and the relationships that include it, the digital signature relationship type from the SignatureOrigin part, the PrintTicket part and the relationships that include it, and the DiscardControl part and the relationships that include it are all signed.

<div class="alert"><b>Note</b>  <p class="note">Setting the <b>XPS_SIGN_POLICY_ALL</b> sets the <b>XPS_SIGN_POLICY_SIGNATURE_RELATIONSHIPS</b> flag, which will cause the signature relationships that start from the signature origin part to be signed. Signatures that are made with this flag set will break when new signatures are added later, because new  signatures  add new signature relationships.

</div>
<div> </div>

## -remarks



More than one value may be set.




## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

