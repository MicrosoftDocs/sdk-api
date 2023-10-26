---
UID: NF:xpsobjectmodel.IXpsOMPath.SetSnapsToPixels
title: IXpsOMPath::SetSnapsToPixels (xpsobjectmodel.h)
description: Sets a Boolean value that indicates whether the path will be snapped to device pixels when that path is being rendered.
helpviewer_keywords: ["FALSE","IXpsOMPath interface [XPS Documents and Packaging]","SetSnapsToPixels method","IXpsOMPath.SetSnapsToPixels","IXpsOMPath::SetSnapsToPixels","SetSnapsToPixels","SetSnapsToPixels method [XPS Documents and Packaging]","SetSnapsToPixels method [XPS Documents and Packaging]","IXpsOMPath interface","TRUE","xps.ixpsompath_setsnapstopixels","xpsobjectmodel/IXpsOMPath::SetSnapsToPixels"]
old-location: xps\ixpsompath_setsnapstopixels.htm
tech.root: xps
ms.assetid: 6b063829-3941-42be-bbe2-49b5a71b695a
ms.date: 12/05/2018
ms.keywords: FALSE, IXpsOMPath interface [XPS Documents and Packaging],SetSnapsToPixels method, IXpsOMPath.SetSnapsToPixels, IXpsOMPath::SetSnapsToPixels, SetSnapsToPixels, SetSnapsToPixels method [XPS Documents and Packaging], SetSnapsToPixels method [XPS Documents and Packaging],IXpsOMPath interface, TRUE, xps.ixpsompath_setsnapstopixels, xpsobjectmodel/IXpsOMPath::SetSnapsToPixels
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
 - IXpsOMPath::SetSnapsToPixels
 - xpsobjectmodel/IXpsOMPath::SetSnapsToPixels
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
 - IXpsOMPath.SetSnapsToPixels
---

# IXpsOMPath::SetSnapsToPixels


## -description

Sets a Boolean value that indicates whether the path will be snapped to device pixels when that path is being rendered.

## -parameters

### -param snapsToPixels [in]

A Boolean value that indicates whether to snap the path to the device pixels when that path is being rendered. The following table describes the values possible for this parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Snap the path to the device pixels.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not snap the path to the device pixels.

</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>