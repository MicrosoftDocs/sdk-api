---
UID: NN:certview.IEnumCERTVIEWCOLUMN
title: IEnumCERTVIEWCOLUMN (certview.h)
author: windows-sdk-content
description: Represents a column-enumeration sequence that contains the column data for the current row of the enumeration sequence.
old-location: security\ienumcertviewcolumn.htm
tech.root: SecCrypto
ms.assetid: 6e6547f9-44b2-4050-be90-ac8ede892adc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumCERTVIEWCOLUMN, IEnumCERTVIEWCOLUMN interface [Security], IEnumCERTVIEWCOLUMN interface [Security],described, _certsrv_ienumcertviewcolumn, certview/IEnumCERTVIEWCOLUMN, security.ienumcertviewcolumn
ms.topic: interface
f1_keywords: ["certview/IEnumCERTVIEWCOLUMN"]
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
 - IEnumCERTVIEWCOLUMN
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumCERTVIEWCOLUMN interface


## -description


The <b>IEnumCERTVIEWCOLUMN</b> interface represents a column-enumeration sequence that contains the column data for the current row of the enumeration sequence.

The column-enumeration sequence is obtained by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewcolumn">IEnumCERTVIEWROW::EnumCertViewColumn</a> method. After this enumeration sequence is obtained, the methods of the <b>IEnumCERTVIEWCOLUMN</b> interface can be used to perform the following tasks:<ul>
<li>Navigate through the enumeration.</li>
<li>Retrieve  data from each column.</li>
<li>Clone an exact copy of the enumeration sequence.</li>
</ul>


<b>IEnumCERTVIEWCOLUMN</b> is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>IEnumCERTVIEWCOLUMN</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumCERTVIEWCOLUMN</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEnumCERTVIEWCOLUMN</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumCERTVIEWCOLUMN</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getdisplayname">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the localized name of the current column in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getmaxlength">GetMaxLength</a>
</td>
<td align="left" width="63%">
Retrieves the maximum allowable length, in bytes, for the column data.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the nonlocalized name of the current column in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the data type of the current column in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the data value contained in the current column in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-isindexed">IsIndexed</a>
</td>
<td align="left" width="63%">
Reports whether the data in the column is indexed.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-next">Next</a>
</td>
<td align="left" width="63%">
Moves to the next column in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-reset">Reset</a>
</td>
<td align="left" width="63%">
Moves to the beginning of  the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewcolumn-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of columns in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-enumcertviewcolumn">ICertView::EnumCertViewColumn</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewrow-enumcertviewcolumn">IEnumCERTVIEWROW::EnumCertViewColumn</a>
 

 

