---
UID: NF:xpsobjectmodel.IXpsOMPart.SetPartName
title: IXpsOMPart::SetPartName (xpsobjectmodel.h)
description: Sets the name that will be used when the part is serialized.
helpviewer_keywords: ["IXpsOMPart interface [XPS Documents and Packaging]","SetPartName method","IXpsOMPart.SetPartName","IXpsOMPart::SetPartName","SetPartName","SetPartName method [XPS Documents and Packaging]","SetPartName method [XPS Documents and Packaging]","IXpsOMPart interface","xps.ixpsompart_setpartname","xpsobjectmodel/IXpsOMPart::SetPartName"]
old-location: xps\ixpsompart_setpartname.htm
tech.root: xps
ms.assetid: d17083f3-38b2-43bd-8e87-1092cf397f29
ms.date: 12/05/2018
ms.keywords: IXpsOMPart interface [XPS Documents and Packaging],SetPartName method, IXpsOMPart.SetPartName, IXpsOMPart::SetPartName, SetPartName, SetPartName method [XPS Documents and Packaging], SetPartName method [XPS Documents and Packaging],IXpsOMPart interface, xps.ixpsompart_setpartname, xpsobjectmodel/IXpsOMPart::SetPartName
f1_keywords:
- xpsobjectmodel/IXpsOMPart.SetPartName
dev_langs:
- c++
req.header: xpsobjectmodel.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsobjectmodel.h
api_name:
- IXpsOMPart.SetPartName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPart::SetPartName


## -description


Sets the name that will be used when the part is serialized.


## -parameters




### -param partUri [in]

A pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>  interface that contains the name of this part. This parameter cannot be <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>partUri</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> will generate an error if it encounters an XPS document part whose name is the same as that of a  part it has previously serialized.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart">IXpsOMPart</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

