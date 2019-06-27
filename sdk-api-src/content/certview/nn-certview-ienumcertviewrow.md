---
UID: NN:certview.IEnumCERTVIEWROW
title: IEnumCERTVIEWROW (certview.h)
author: windows-sdk-content
description: Represents a row-enumeration sequence that contains the data in the rows of the Certificate Services view, allowing further access to the columns, attributes, and extensions associated with each row.
old-location: security\ienumcertviewrow.htm
tech.root: SecCrypto
ms.assetid: c9529f7a-9d97-4315-af96-f7b687af3c2e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWROW, IEnumCERTVIEWROW interface [Security], IEnumCERTVIEWROW interface [Security],described, _certsrv_ienumcertviewrow, certview/IEnumCERTVIEWROW, security.ienumcertviewrow
ms.topic: interface
f1_keywords: 
 - "certview/IEnumCERTVIEWROW"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IEnumCERTVIEWROW
 - IEnumCERTVIEWROW.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumCERTVIEWROW interface


## -description


The <b>IEnumCERTVIEWROW</b> interface represents a row-enumeration sequence that contains the data in the rows of the Certificate Services view, allowing further access to the columns, attributes, and extensions associated with each row.

The row-enumeration sequence is obtained through a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-openview">ICertView::OpenView</a> method. After this enumeration sequence is obtained, the <b>IEnumCERTVIEWROW</b> methods can be used to perform the following tasks:<ul>
<li>Navigate through the enumeration sequence.</li>
<li>Obtain other objects for enumerating the columns, certificate extensions, or attributes associated with a specific row.</li>
<li>Retrieve the maximum number of rows for the view.</li>
</ul>


<b>IEnumCERTVIEWROW</b> is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>IEnumCERTVIEWROW</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumCERTVIEWROW</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEnumCERTVIEWROW</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumCERTVIEWROW</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>Clone</b></td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewattribute">EnumCertViewAttribute</a>
</td>
<td align="left" width="63%">
Obtains an instance of an attribute-enumeration sequence for the current row of the row-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWROW</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewcolumn">EnumCertViewColumn</a>
</td>
<td align="left" width="63%">
Obtains an instance of a column-enumeration sequence for the current row of the row-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWROW</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewextension">EnumCertViewExtension</a>
</td>
<td align="left" width="63%">
Obtains an instance of an extension-enumeration sequence for the current row of the row-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWROW</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewrow-getmaxindex">GetMaxIndex</a>
</td>
<td align="left" width="63%">
Retrieves the maximum valid index value after all the rows in the row-enumeration sequence have been referenced.</p> (Inherited from <b>IEnumCERTVIEWROW</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">Next</a>
</td>
<td align="left" width="63%">
Moves to the next row in the row-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWROW</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewrow-reset">Reset</a>
</td>
<td align="left" width="63%">
Moves to the beginning of the row-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWROW</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewrow-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of rows in the row-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWROW</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-openview">ICertView</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

