---
UID: NF:xpsobjectmodel.IXpsOMPage.SetLanguage
title: IXpsOMPage::SetLanguage
author: windows-sdk-content
description: Sets the Language property of the page.
old-location: xps\ixpsompage_setlanguage.htm
old-project: printdocs
ms.assetid: 3bf0c7ed-84fc-45c0-8058-b833c3913f09
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetLanguage method, IXpsOMPage.SetLanguage, IXpsOMPage::SetLanguage, SetLanguage, SetLanguage method [XPS Documents and Packaging], SetLanguage method [XPS Documents and Packaging],IXpsOMPage interface, xps.ixpsompage_setlanguage, xpsobjectmodel/IXpsOMPage::SetLanguage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMPage.SetLanguage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPage::SetLanguage


## -description


Sets the <b>Language</b> property of the page.


## -parameters




### -param language [in]

A language tag string that represents the language of the page content. A <b>NULL</b> pointer clears the previously assigned language.


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
<dt><b>XPS_E_INVALID_LANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
The language string contains one or more language strings that are not valid. 

</td>
</tr>
</table>
 




## -remarks



The language tag string must conform to the language tag syntax that is described in the Internet Engineering Task Force (IETF) RFC 3066. For more information,  go to <a href="http://go.microsoft.com/fwlink/p/?linkid=161490">http://tools.ietf.org/html/rfc3066</a>. 




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=161490">The Internet Engineering Task Force (IETF) RFC 3066</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

