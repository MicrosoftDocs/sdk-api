---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetIsHyperlinkTarget
title: IXpsOMVisual::SetIsHyperlinkTarget (xpsobjectmodel.h)
author: windows-sdk-content
description: Specifies whether the visual is the target of a hyperlink.
old-location: xps\ixpsomvisual_setishyperlinktarget.htm
tech.root: printdocs
ms.assetid: 855a3993-b308-4dc0-a2f6-8ac6bdc495ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FALSE, IXpsOMVisual interface [XPS Documents and Packaging],SetIsHyperlinkTarget method, IXpsOMVisual.SetIsHyperlinkTarget, IXpsOMVisual::SetIsHyperlinkTarget, SetIsHyperlinkTarget, SetIsHyperlinkTarget method [XPS Documents and Packaging], SetIsHyperlinkTarget method [XPS Documents and Packaging],IXpsOMVisual interface, TRUE, xps.ixpsomvisual_setishyperlinktarget, xpsobjectmodel/IXpsOMVisual::SetIsHyperlinkTarget
ms.topic: method
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
 - IXpsOMVisual.SetIsHyperlinkTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMVisual::SetIsHyperlinkTarget


## -description


Specifies whether the visual is the target of a hyperlink.


## -parameters




### -param isHyperlink [in]

The Boolean value that specifies whether the visual is the target of a hyperlink.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The visual is the target of a hyperlink.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The visual is not the target of a hyperlink.

</td>
</tr>
</table>
 


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
<dt><b>XPS_E_MISSING_NAME</b></dt>
</dl>
</td>
<td width="60%">
The page has not been named. The hyperlink target status can only be set if the page has a name.

</td>
</tr>
</table>
 




## -remarks



The visual must be named before it can  be set as the target of a  hyperlink.




## -see-also




<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="https://msdn.microsoft.com/8bf30b4c-bddf-4ca8-91c6-af739125829c">SetName</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

