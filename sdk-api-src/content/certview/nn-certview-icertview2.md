---
UID: NN:certview.ICertView2
title: ICertView2
author: windows-sdk-content
description: Allow properly authorized clients to create a customized or complete view of the Certificate Services database.
old-location: security\icertview2.htm
tech.root: seccrypto
ms.assetid: c29f1db3-0cdf-463e-a202-47fbba8e1c81
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICertView2, ICertView2 interface [Security], ICertView2 interface [Security],described, _certsrv_icertview2, certview/ICertView2, security.icertview2
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
 - ICertView2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


In C++, the <b>ICertView2</b> interface is instantiated through a call to the COM function <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>. If, on the other hand, you are using Visual Basic Scripting Edition, you will need to reference the CertAdm Type library in your project and then instantiate the <b>CCertView</b> object by a call to 'New'.  The sample code for the  
<a href="https://msdn.microsoft.com/en-us/library/Aa385432(v=VS.85).aspx">OpenConnection</a> method illustrates the instantiation techniques.

The <b>ICertView2</b> interface is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>ICertView2</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertView2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a> and <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>. <b>ICertView2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa385422(v=VS.85).aspx">EnumCertViewColumn</a>
</td>
<td align="left" width="63%">
Obtains a pointer to 
<a href="https://msdn.microsoft.com/en-us/library/Aa386176(v=VS.85).aspx">IEnumCERTVIEWCOLUMN</a> for schema enumeration.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385424(v=VS.85).aspx">GetColumnCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of columns in the view.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d869db9-b4df-4fcd-85e7-19fe773b4262">GetColumnIndex</a>
</td>
<td align="left" width="63%">
Retrieves the zero-based index of a named column.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385432(v=VS.85).aspx">OpenConnection</a>
</td>
<td align="left" width="63%">
Establishes an instance of a column-enumeration sequence for the database schema.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385435(v=VS.85).aspx">OpenView</a>
</td>
<td align="left" width="63%">
Opens a view to a Certificate Services database and instantiates an instance of an 
<a href="https://msdn.microsoft.com/en-us/library/Aa386231(v=VS.85).aspx">IEnumCERTVIEWROW</a> object.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385439(v=VS.85).aspx">SetRestriction</a>
</td>
<td align="left" width="63%">
Sets sorting and qualifying restrictions on a column.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385442(v=VS.85).aspx">SetResultColumn</a>
</td>
<td align="left" width="63%">
Specifies a column for the result set of a customized view of the Certificate Services database.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385450(v=VS.85).aspx">SetResultColumnCount</a>
</td>
<td align="left" width="63%">
Specifies the maximum the number of columns for the result set of a customized view of the Certificate Services database.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">CCertView</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385452(v=VS.85).aspx">SetTable</a>
</td>
<td align="left" width="63%">
Specifies which Certificate Services database table is used for subsequent calls to  the methods of the <b>ICertView2</b> interface.</p> (Inherited from <b>ICertView2</b><b>CCertView</b>)</td>
</tr>
</table> 

