---
UID: NN:certview.ICertView2
title: ICertView2 (certview.h)
description: Allow properly authorized clients to create a customized or complete view of the Certificate Services database.
helpviewer_keywords: ["ICertView2","ICertView2 interface [Security]","ICertView2 interface [Security]","described","_certsrv_icertview2","certview/ICertView2","security.icertview2"]
old-location: security\icertview2.htm
tech.root: security
ms.assetid: c29f1db3-0cdf-463e-a202-47fbba8e1c81
ms.date: 12/05/2018
ms.keywords: ICertView2, ICertView2 interface [Security], ICertView2 interface [Security],described, _certsrv_icertview2, certview/ICertView2, security.icertview2
f1_keywords:
- certview/ICertView2
dev_langs:
- c++
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
- ICertView2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertView2 interface


## -description


The <b>ICertView2</b> interface is one of two interfaces that allow properly authorized clients to create a customized or complete view of the Certificate Services database.

The <b>ICertView2</b> interface is used to perform the following tasks:<ul>
<li>Establish a connection with a Certificate Services server.</li>
<li>Obtain a row-enumeration sequence of the rows in the Certificate Services database.</li>
<li>Obtain a column-enumeration sequence for the schema in the Certificate Services database.</li>
<li>Get the column count and index.</li>
<li>Specify sorting and qualifying restrictions for a column.</li>
<li>Specify the number of columns and a specific column in a customized view.</li>
<li>Specify which tables are used by subsequent calls to <b>ICertView2</b> methods (introduced by <b>ICertView2</b>).</li>
</ul>


In C++, the <b>ICertView2</b> interface is instantiated through a call to the COM function <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. If, on the other hand, you are using Visual Basic Scripting Edition, you will need to reference the CertAdm Type library in your project and then instantiate the <b>CCertView</b> object by a call to 'New'.  The sample code for the  
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-openconnection">OpenConnection</a> method illustrates the instantiation techniques.

The <b>ICertView2</b> interface is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>ICertView2</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertView2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">ICertView</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. <b>ICertView2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertView2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-enumcertviewcolumn">EnumCertViewColumn</a>
</td>
<td align="left" width="63%">
Obtains a pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-ienumcertviewcolumn">IEnumCERTVIEWCOLUMN</a> for schema enumeration.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-getcolumncount">GetColumnCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of columns in the view.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-getcolumnindex">GetColumnIndex</a>
</td>
<td align="left" width="63%">
Retrieves the zero-based index of a named column.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-openconnection">OpenConnection</a>
</td>
<td align="left" width="63%">
Establishes an instance of a column-enumeration sequence for the database schema.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-openview">OpenView</a>
</td>
<td align="left" width="63%">
Opens a view to a Certificate Services database and instantiates an instance of an 
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a> object.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-setrestriction">SetRestriction</a>
</td>
<td align="left" width="63%">
Sets sorting and qualifying restrictions on a column.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-setresultcolumn">SetResultColumn</a>
</td>
<td align="left" width="63%">
Specifies a column for the result set of a customized view of the Certificate Services database.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-setresultcolumncount">SetResultColumnCount</a>
</td>
<td align="left" width="63%">
Specifies the maximum the number of columns for the result set of a customized view of the Certificate Services database.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview2-settable">SetTable</a>
</td>
<td align="left" width="63%">
Specifies which Certificate Services database table is used for subsequent calls to  the methods of the <b>ICertView2</b> interface.</p> (Inherited from <b>ICertView2</b><b>CCertView</b>)</td>
</tr>
</table> 

