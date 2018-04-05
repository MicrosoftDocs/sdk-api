---
UID: NF:xpsobjectmodel.IXpsOMPage.GetOwner
title: IXpsOMPage::GetOwner method
author: windows-driver-content
description: Gets a pointer to the IXpsOMPageReference interface that contains the page.
old-location: xps\ixpsompage_getowner.htm
old-project: printdocs
ms.assetid: fd29eaa7-8f9c-4468-ad3b-a159bf5f516c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging], IXpsOMPage interface, GetOwner,IXpsOMPage.GetOwner, IXpsOMPage, IXpsOMPage interface [XPS Documents and Packaging], GetOwner method, IXpsOMPage::GetOwner, xps.ixpsompage_getowner, xpsobjectmodel/IXpsOMPage::GetOwner
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IXpsOMPage.GetOwner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPage::GetOwner method


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface that contains the page.


## -parameters




### -param pageReference [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface that contains the page.


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
<i>pageReference</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



When the page does not have an owner, a <b>NULL</b> pointer is returned in <i>pageReference</i>.




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

