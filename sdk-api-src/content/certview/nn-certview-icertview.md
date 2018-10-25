---
UID: NN:certview.ICertView
title: ICertView
author: windows-sdk-content
description: Allows properly authorized clients to create a customized or complete view of the Certificate Services database.
old-location: security\icertview.htm
tech.root: seccrypto
ms.assetid: 0b6660ee-458f-457f-8a38-0d950aee2710
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ICertView, ICertView interface [Security], ICertView interface [Security],described, _certsrv_icertview, certview/ICertView, security.icertview
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
 - ICertView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertView interface


## -description


The <b>ICertView</b> interface allows properly authorized clients to create a customized or complete view of the Certificate Services database.

The <b>ICertView</b> interface is used to perform the following tasks:<ul>
<li>Establish a connection with a Certificate Services server.</li>
<li>Obtain a row-enumeration sequence of the rows in the Certificate Services database.</li>
<li>Obtain a column-enumeration sequence for the columns of a row in the Certificate Services database.</li>
<li>Get the column count and index.</li>
<li>Specify sorting and qualifying restrictions for a column.</li>
<li>Specify the number of columns and a specific column in a customized view.</li>
</ul>


In C++, the <b>ICertView</b> interface is instantiated through a call to the COM function <a href="_com_cocreateinstance">CoCreateInstance</a>. If, on the other hand, you are using Visual Basic Scripting Edition, you will need to reference the CertAdm Type library in your project and then instantiate the <a href="https://msdn.microsoft.com/c29f1db3-0cdf-463e-a202-47fbba8e1c81">CCertView</a> object  by a call to 'New'. The sample code for the  
<a href="https://msdn.microsoft.com/576af4d1-88c9-40e3-9438-9fefd483be7a">ICertView::OpenConnection</a> method illustrates the instantiation techniques.

The <b>ICertView</b> interface is defined in Certview.h. When you create your program, however, use Certsrv.h as the include file. Certadm.dll provides the <b>ICertView</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertView</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a51162f9-cc3d-4f06-993a-e5c9f57dd8a1">EnumCertViewColumn</a>
</td>
<td align="left" width="63%">
Obtains a pointer to 
<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a> for schema enumeration.</p> (Inherited from <b>ICertView</b><b>CCertView</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0297d8e3-5077-40da-88b7-adac252e0f1b">GetColumnCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of columns in the view.</p> (Inherited from <b>ICertView</b><b>CCertView</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d869db9-b4df-4fcd-85e7-19fe773b4262">GetColumnIndex</a>
</td>
<td align="left" width="63%">
Retrieves the zero-based index of a named column.</p> (Inherited from <b>ICertView</b><b>CCertView</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/576af4d1-88c9-40e3-9438-9fefd483be7a">OpenConnection</a>
</td>
<td align="left" width="63%">
Establishes a connection with a Certificate Services server.</p> (Inherited from <b>ICertView</b><b>CCertView</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d68a5463-f711-4737-b0ad-889f7e4855d5">OpenView</a>
</td>
<td align="left" width="63%">
Opens a view to a Certificate Services database and obtains a pointer to 
<a href="https://msdn.microsoft.com/c9529f7a-9d97-4315-af96-f7b687af3c2e">IEnumCERTVIEWROW</a>.</p> (Inherited from <b>ICertView</b><b>CCertView</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2dc8675-1d75-4c15-a9f7-971274ab044c">SetRestriction</a>
</td>
<td align="left" width="63%">
Sets sorting and qualifying restrictions on a column.</p> (Inherited from <b>ICertView</b><b>CCertView</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c13bdc3a-e623-49df-bba0-34c4c178dc3b">SetResultColumn</a>
</td>
<td align="left" width="63%">
Specifies a column for the result set of a customized view of the Certificate Services database.</p> (Inherited from <b>ICertView</b><b>CCertView</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f98b2f45-be9f-47ba-9c6b-63a2912288ac">SetResultColumnCount</a>
</td>
<td align="left" width="63%">
Specifies the maximum the number of columns for the result set of a customized view of the Certificate Services database.</p> (Inherited from <b>ICertView</b><b>CCertView</b>)</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/c9529f7a-9d97-4315-af96-f7b687af3c2e">IEnumCERTVIEWROW</a>
 

 

