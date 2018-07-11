---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetName
title: IXpsOMVisual::SetName
author: windows-sdk-content
description: Sets the Name property of the visual.
old-location: xps\ixpsomvisual_setname.htm
old-project: printdocs
ms.assetid: 8bf30b4c-bddf-4ca8-91c6-af739125829c
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetName method, IXpsOMVisual.SetName, IXpsOMVisual::SetName, SetName, SetName method [XPS Documents and Packaging], SetName method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_setname, xpsobjectmodel/IXpsOMVisual::SetName
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
 - IXpsOMVisual.SetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMVisual::SetName


## -description



        Sets the <b>Name</b>  property of the visual.
      


## -parameters




### -param name [in]


            The name of the visual. A <b>NULL</b> pointer clears the <b>Name</b> property.
          


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
<dt><b>XPS_E_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">

                According to the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>, the string that is passed in <i>name</i>  is not a valid name.
              

</td>
</tr>
</table>
 




## -remarks



Names must be unique.


        Clearing the <b>Name</b> property by passing a <b>NULL</b> pointer in <i>name</i> sets the <b>IsHyperlinkTarget</b> property to <b>FALSE</b>.
      




## -see-also




<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

