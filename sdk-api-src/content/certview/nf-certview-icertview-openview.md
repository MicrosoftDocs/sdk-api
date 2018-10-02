---
UID: NF:certview.ICertView.OpenView
title: ICertView::OpenView
author: windows-sdk-content
description: Opens a view to a Certificate Services database and instantiates an instance of an IEnumCERTVIEWROW object.
old-location: security\icertview2_openview.htm
tech.root: seccrypto
ms.assetid: d68a5463-f711-4737-b0ad-889f7e4855d5
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CCertView object [Security],OpenView method, ICertView interface [Security],OpenView method, ICertView.OpenView, ICertView2 interface [Security],OpenView method, ICertView2::OpenView, ICertView::OpenView, OpenView, OpenView method [Security], OpenView method [Security],CCertView object, OpenView method [Security],ICertView interface, OpenView method [Security],ICertView2 interface, certview/ICertView2::OpenView, certview/ICertView::OpenView, security.icertview2_openview
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ICertView2.OpenView
 - ICertView.OpenView
 - CCertView.OpenView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertView::OpenView


## -description


The <b>OpenView</b> method opens a view to a Certificate Services database and instantiates an instance of an <a href="https://msdn.microsoft.com/en-us/library/Aa386231(v=VS.85).aspx">IEnumCERTVIEWROW</a> object.


## -parameters




### -param ppenum [out]

A pointer to a pointer of <a href="https://msdn.microsoft.com/en-us/library/Aa386231(v=VS.85).aspx">IEnumCERTVIEWROW</a> type.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is an <a href="https://msdn.microsoft.com/en-us/library/Aa386231(v=VS.85).aspx">IEnumCERTVIEWROW</a> object.




## -remarks



Before calling the <b>OpenView</b> method, it is necessary to establish a connection with a Certificate Services server by calling the 
<a href="https://msdn.microsoft.com/en-us/library/Aa385432(v=VS.85).aspx">OpenConnection</a> method first.

The 
<a href="https://msdn.microsoft.com/en-us/library/Aa386231(v=VS.85).aspx">IEnumCERTVIEWROW</a> object returned by this call represents a row-enumeration sequence whose internal index is pointing to the beginning of the sequence. To look at the first row in the sequence, call the  
<a href="https://msdn.microsoft.com/en-us/library/Aa386249(v=VS.85).aspx">IEnumCERTVIEWROW::Next</a> method, which moves the internal index to the first row.

To view a nondefault column set or a subset of the rows, call 
<a href="https://msdn.microsoft.com/en-us/library/Aa385450(v=VS.85).aspx">SetResultColumnCount</a>, 
<a href="https://msdn.microsoft.com/en-us/library/Aa385442(v=VS.85).aspx">SetResultColumn</a>, and 
<a href="https://msdn.microsoft.com/en-us/library/Aa385439(v=VS.85).aspx">SetRestriction</a> after calling <a href="https://msdn.microsoft.com/en-us/library/Aa385432(v=VS.85).aspx">OpenConnection</a> and before calling <b>OpenView</b>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pCertView is previously instantiated pointer to ICertView.
IEnumCERTVIEWROW * pEnumRow = NULL;
HRESULT    hr;

hr = pCertView-&gt;OpenView(&amp;pEnumRow);
if (S_OK != hr)
    printf("Failed ICertView::OpenView - %x\n", hr);
else
    // use pEnumRow as needed, to enumerate data rows
    // ...
// Done processing, free resources.
if (NULL != pEnumRow)
    pEnumRow-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385414(v=VS.85).aspx">ICertView</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385417(v=VS.85).aspx">ICertView2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385432(v=VS.85).aspx">ICertView::OpenConnection</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386231(v=VS.85).aspx">IEnumCERTVIEWROW</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386249(v=VS.85).aspx">IEnumCERTVIEWROW::Next</a>
 

 

