---
UID: NF:xpsobjectmodel.IXpsOMPath.GetSnapsToPixels
title: IXpsOMPath::GetSnapsToPixels (xpsobjectmodel.h)
description: Gets a Boolean value that indicates whether the path is to be snapped to device pixels when the path is rendered.
helpviewer_keywords: ["FALSE","GetSnapsToPixels","GetSnapsToPixels method [XPS Documents and Packaging]","GetSnapsToPixels method [XPS Documents and Packaging]","IXpsOMPath interface","IXpsOMPath interface [XPS Documents and Packaging]","GetSnapsToPixels method","IXpsOMPath.GetSnapsToPixels","IXpsOMPath::GetSnapsToPixels","TRUE","xps.ixpsompath_getsnapstopixels","xpsobjectmodel/IXpsOMPath::GetSnapsToPixels"]
old-location: xps\ixpsompath_getsnapstopixels.htm
tech.root: xps
ms.assetid: c0a4a8b5-f7cf-4cbe-9221-41cde4f63557
ms.date: 12/05/2018
ms.keywords: FALSE, GetSnapsToPixels, GetSnapsToPixels method [XPS Documents and Packaging], GetSnapsToPixels method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetSnapsToPixels method, IXpsOMPath.GetSnapsToPixels, IXpsOMPath::GetSnapsToPixels, TRUE, xps.ixpsompath_getsnapstopixels, xpsobjectmodel/IXpsOMPath::GetSnapsToPixels
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
 - IXpsOMPath::GetSnapsToPixels
 - xpsobjectmodel/IXpsOMPath::GetSnapsToPixels
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
 - IXpsOMPath.GetSnapsToPixels
---

# IXpsOMPath::GetSnapsToPixels


## -description

Gets a Boolean value that indicates whether the path is to  be snapped to device pixels when the path is rendered.

## -parameters

### -param snapsToPixels [out, retval]

A Boolean value that indicates whether the path is to be snapped to device pixels when the path is rendered. The following table describes the values possible  for this parameter.

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
The path is to be snapped to device pixels.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The path is not to be snapped to device pixels.

</td>
</tr>
</table>

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>snapsToPixels</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The value returned by <b>GetSnapsToPixels</b> corresponds to the <b>SnapsToDevicePixels</b> element in the document markup.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>