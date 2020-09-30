---
UID: NN:certview.IEnumCERTVIEWEXTENSION
title: IEnumCERTVIEWEXTENSION (certview.h)
description: Represents an extension-enumeration sequence that contains the certificate extension data for the current row of the row-enumeration sequence.
helpviewer_keywords: ["IEnumCERTVIEWEXTENSION","IEnumCERTVIEWEXTENSION interface [Security]","IEnumCERTVIEWEXTENSION interface [Security]","described","_certsrv_ienumcertviewextension","certview/IEnumCERTVIEWEXTENSION","security.ienumcertviewextension"]
old-location: security\ienumcertviewextension.htm
tech.root: security
ms.assetid: d5acff51-06f8-4a6f-aa9e-97ba052b1b34
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWEXTENSION, IEnumCERTVIEWEXTENSION interface [Security], IEnumCERTVIEWEXTENSION interface [Security],described, _certsrv_ienumcertviewextension, certview/IEnumCERTVIEWEXTENSION, security.ienumcertviewextension
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
 - IEnumCERTVIEWEXTENSION
 - certview/IEnumCERTVIEWEXTENSION
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
 - IEnumCERTVIEWEXTENSION
---

# IEnumCERTVIEWEXTENSION interface


## -description

The <b>IEnumCERTVIEWEXTENSION</b> interface represents an extension-enumeration sequence that contains the  certificate extension data for the current row of the row-enumeration sequence.

 The extension-enumeration sequence is obtained by a call to the   
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewextension">IEnumCERTVIEWROW::EnumCertViewExtension</a> method. After this enumeration sequence is obtained, the methods of the <b>IEnumCERTVIEWEXTENSION</b> interface can be used to perform the following tasks:<ul>
<li>Navigate the extension-enumeration sequence.</li>
<li>Retrieve the name, value, and flags of the extension in the enumeration.</li>
<li>Clone an exact copy of the extension-enumeration sequence.</li>
</ul>


<b>IEnumCERTVIEWEXTENSION</b> is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>IEnumCERTVIEWEXTENSION</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumCERTVIEWEXTENSION</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEnumCERTVIEWEXTENSION</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumCERTVIEWEXTENSION</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves the policy and origin flags of the current extension in the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current extension in the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of the current extension in the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-next">Next</a>
</td>
<td align="left" width="63%">
Moves to the next extension in the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-reset">Reset</a>
</td>
<td align="left" width="63%">
Moves to the beginning of the extension-enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewextension-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of extensions in the extension-enumeration sequence.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewextension">IEnumCERTVIEWROW::IEnumCertViewExtension</a>