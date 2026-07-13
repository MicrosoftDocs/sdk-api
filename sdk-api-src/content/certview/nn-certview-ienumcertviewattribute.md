---
UID: NN:certview.IEnumCERTVIEWATTRIBUTE
title: IEnumCERTVIEWATTRIBUTE (certview.h)
description: Represents an attribute-enumeration sequence that contains the certificate attributes for the current row of the row-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWATTRIBUTE","IEnumCERTVIEWATTRIBUTE interface [Security]","IEnumCERTVIEWATTRIBUTE interface [Security]","described","_certsrv_ienumcertviewattribute","certview/IEnumCERTVIEWATTRIBUTE","security.ienumcertviewattribute"]
old-location: security\ienumcertviewattribute.htm
tech.root: security
ms.assetid: fc1eb29d-27d9-4331-b588-dc0632b3db6a
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWATTRIBUTE, IEnumCERTVIEWATTRIBUTE interface [Security], IEnumCERTVIEWATTRIBUTE interface [Security],described, _certsrv_ienumcertviewattribute, certview/IEnumCERTVIEWATTRIBUTE, security.ienumcertviewattribute
req.header: certview.h
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
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumCERTVIEWATTRIBUTE
 - certview/IEnumCERTVIEWATTRIBUTE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IEnumCERTVIEWATTRIBUTE
---

# IEnumCERTVIEWATTRIBUTE interface


## -description

The <b>IEnumCERTVIEWATTRIBUTE</b> interface represents an attribute-enumeration sequence that contains the   certificate attributes for the current row of the row-enumeration sequence.

The attribute-enumeration sequence is obtained by a call to 
the <a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewattribute">IEnumCERTVIEWROW::EnumCertViewAttribute</a> method. After this enumeration sequence is obtained, the methods of the <b>IEnumCERTVIEWATTRIBUTE</b> interface can be used to perform the following tasks:<ul>
<li>Navigate through the enumeration of certificate attributes.</li>
<li>Retrieve the name and value of the attributes in the enumeration.</li>
<li>Clone an exact copy of the certificate attribute object.</li>
</ul>


<b>IEnumCERTVIEWATTRIBUTE</b> is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>IEnumCERTVIEWATTRIBUTE</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>IEnumCERTVIEWATTRIBUTE</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEnumCERTVIEWATTRIBUTE</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewattribute">IEnumCERTVIEWROW::EnumCertViewAttribute</a>
