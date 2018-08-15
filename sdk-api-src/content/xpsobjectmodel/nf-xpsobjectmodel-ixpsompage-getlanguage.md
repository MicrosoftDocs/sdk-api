---
UID: NF:xpsobjectmodel.IXpsOMPage.GetLanguage
title: IXpsOMPage::GetLanguage
author: windows-sdk-content
description: Gets the Language property of the page.
old-location: xps\ixpsompage_getlanguage.htm
old-project: printdocs
ms.assetid: d16378cc-dd1c-49f9-9c1b-1eb0d78067f7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetLanguage, GetLanguage method [XPS Documents and Packaging], GetLanguage method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetLanguage method, IXpsOMPage.GetLanguage, IXpsOMPage::GetLanguage, xps.ixpsompage_getlanguage, xpsobjectmodel/IXpsOMPage::GetLanguage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPage.GetLanguage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPage::GetLanguage


## -description


Gets the <b>Language</b> property of the page.


## -parameters




### -param language [out, retval]

A language tag string that represents the language of the page contents. If the <b>Language</b> property has not been set, a <b>NULL</b> pointer is returned.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>language</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The default value is the language tag string that is passed to <a href="https://msdn.microsoft.com/9212ccd8-0793-40cc-bab5-609ea74715f7">IXpsOMObjectFactory::CreatePage</a>  in the <i>language</i>  parameter.

Internet Engineering Task Force (IETF) RFC 3066 describes the recommended encoding of the language tag string that is returned in <i>language</i>.

This method allocates the memory used by the string that is returned in <i>language</i>.  If <i>language</i> is not <b>NULL</b>, use the <a href="_com_CoTaskMemFree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=161490">The Internet Engineering Task Force (IETF) RFC 3066</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

