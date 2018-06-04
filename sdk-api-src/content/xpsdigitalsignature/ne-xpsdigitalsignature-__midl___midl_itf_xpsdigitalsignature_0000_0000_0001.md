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

# __MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0001 enumeration


## -description


Describes the status of a document's digital signature.


## -enum-fields




### -field XPS_SIGNATURE_STATUS_INCOMPLIANT

The signature violates one or more  signing rules stated in section 10.2.1.2 of the   <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>. These rules describe the parts or relationships that must or must not be signed.

A signature that is incompliant must be created as such. 
Changing signed content cannot make a valid signature incompliant. One example of an incompliant signature  is the signature of a   package that has an unknown relationships type at the root.


### -field XPS_SIGNATURE_STATUS_INCOMPLETE

The signature does not include parts that must be signed.

If a valid XPS signature is created and the XPS document contents are later modified, the signature will become incomplete or broken.
For example, removing a page from a FixedDocument makes the signature incomplete; it also breaks the signature,  but  the fact that the signature is incomplete is of greater importance.


### -field XPS_SIGNATURE_STATUS_BROKEN

This is a compliant digital signature, but it fails the signature validation routines described in the <i>Open Packaging Conventions</i> (refer to See Also).

Modification of the markup in a FixedPage that has been signed breaks the signature.


### -field XPS_SIGNATURE_STATUS_QUESTIONABLE

This is not an incompliant or broken digital signature, but the signed content (parts and relationships) includes elements or attributes from an unknown namespace introduced through the markup compatibility mechanisms.


### -field XPS_SIGNATURE_STATUS_VALID

This is a valid signature: it is not broken, incompliant, or questionable. The application, however,  must still check the certificate trust chain, revocation lists, and expiration dates.


## -remarks



The digital signature status values correspond to section 10.2.1.2 in the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.

The Open Packaging Conventions are specified in   the 1st edition, Part 2, "Open Packaging Conventions," of <a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>.

<div class="alert"><b>Note</b>  These resources may not be available in some languages 

and countries.</div>
<div> </div>



## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

