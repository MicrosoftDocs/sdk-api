---
UID: NN:certview.IEnumCERTVIEWCOLUMN
title: IEnumCERTVIEWCOLUMN
author: windows-sdk-content
description: Represents a column-enumeration sequence that contains the column data for the current row of the enumeration sequence.
old-location: security\ienumcertviewcolumn.htm
tech.root: seccrypto
ms.assetid: 6e6547f9-44b2-4050-be90-ac8ede892adc
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IEnumCERTVIEWCOLUMN, IEnumCERTVIEWCOLUMN interface [Security], IEnumCERTVIEWCOLUMN interface [Security],described, _certsrv_ienumcertviewcolumn, certview/IEnumCERTVIEWCOLUMN, security.ienumcertviewcolumn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IEnumCERTVIEWCOLUMN interface


## -description


The <b>IEnumCERTVIEWCOLUMN</b> interface represents a column-enumeration sequence that contains the column data for the current row of the enumeration sequence.

The column-enumeration sequence is obtained by a call to the <a href="https://msdn.microsoft.com/78fd2431-c4c7-4df9-856a-69665fa8c063">IEnumCERTVIEWROW::EnumCertViewColumn</a> method. After this enumeration sequence is obtained, the methods of the <b>IEnumCERTVIEWCOLUMN</b> interface can be used to perform the following tasks:<ul>
<li>Navigate through the enumeration.</li>
<li>Retrieve  data from each column.</li>
<li>Clone an exact copy of the enumeration sequence.</li>
</ul>


<b>IEnumCERTVIEWCOLUMN</b> is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>IEnumCERTVIEWCOLUMN</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumCERTVIEWCOLUMN</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IEnumCERTVIEWCOLUMN</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a0870155-3f16-4cfb-b180-7a8e617dfcd8">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7fd06f7-7b42-47ed-be03-867d0d03594a">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the localized name of the current column in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20cd5f5a-2e19-43ca-9b84-70e6dd1a4cad">GetMaxLength</a>
</td>
<td align="left" width="63%">
Retrieves the maximum allowable length, in bytes, for the column data.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be76cec1-9ac0-4cc0-bddb-992b2d3590d7">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the nonlocalized name of the current column in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53297e9e-6583-4edf-85f4-e2b2e4ba28b3">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the data type of the current column in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cc14bd1-7963-4b11-aef6-4ef3b0b7f6c1">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the data value contained in the current column in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7373c0c3-3a1d-4a32-90e6-0f0575a0b61b">IsIndexed</a>
</td>
<td align="left" width="63%">
Reports whether the data in the column is indexed.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c77d1c7-af3a-4a7d-bf42-69be887c881e">Next</a>
</td>
<td align="left" width="63%">
Moves to the next column in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0be00eb0-1a22-4849-95ca-276099bbfa74">Reset</a>
</td>
<td align="left" width="63%">
Moves to the beginning of  the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a101e5b-a137-4e15-81b6-90e0fc14b887">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of columns in the column-enumeration sequence.</p> (Inherited from <b>IEnumCERTVIEWCOLUMN</b><b>IEnumCERTVIEWCOLUMN</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a51162f9-cc3d-4f06-993a-e5c9f57dd8a1">ICertView::EnumCertViewColumn</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/78fd2431-c4c7-4df9-856a-69665fa8c063">IEnumCERTVIEWROW::EnumCertViewColumn</a>
 

 

