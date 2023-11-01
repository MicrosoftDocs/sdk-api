---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetLanguage
title: IXpsOMVisual::SetLanguage (xpsobjectmodel.h)
description: Sets the Language property of the visual.
helpviewer_keywords: ["IXpsOMVisual interface [XPS Documents and Packaging]","SetLanguage method","IXpsOMVisual.SetLanguage","IXpsOMVisual::SetLanguage","SetLanguage","SetLanguage method [XPS Documents and Packaging]","SetLanguage method [XPS Documents and Packaging]","IXpsOMVisual interface","xps.ixpsomvisual_setlanguage","xpsobjectmodel/IXpsOMVisual::SetLanguage"]
old-location: xps\ixpsomvisual_setlanguage.htm
tech.root: xps
ms.assetid: 19a7c10d-ceea-4303-a655-a3cb8b910377
ms.date: 12/05/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetLanguage method, IXpsOMVisual.SetLanguage, IXpsOMVisual::SetLanguage, SetLanguage, SetLanguage method [XPS Documents and Packaging], SetLanguage method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_setlanguage, xpsobjectmodel/IXpsOMVisual::SetLanguage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMVisual::SetLanguage
 - xpsobjectmodel/IXpsOMVisual::SetLanguage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMVisual.SetLanguage
---

# IXpsOMVisual::SetLanguage


## -description

Sets the <b>Language</b> property of the visual.

## -parameters

### -param language [in]

The language string that specifies the language of the visual and of its contents. A <b>NULL</b> pointer clears the   <b>Language</b> property.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
 The value of <i>language</i> is formatted incorrectly or specifies a language that is not valid.

</td>
</tr>
</table>

## -remarks

The recommended encoding for the <b>Language</b> property is specified in Internet Engineering Task Force (IETF) RFC 3066r.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>