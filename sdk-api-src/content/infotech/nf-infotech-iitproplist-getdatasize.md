---
UID: NF:infotech.IITPropList.GetDataSize
title: IITPropList::GetDataSize (infotech.h)
description: Returns the number of bytes needed to save the property data.
helpviewer_keywords: ["GetDataSize","GetDataSize method [HTML Help Workshop]","GetDataSize method [HTML Help Workshop]","IITPropList interface","IITPropList interface [HTML Help Workshop]","GetDataSize method","IITPropList.GetDataSize","IITPropList::GetDataSize","htmlhelp.iitproplist_getdatasize","infotech/IITPropList::GetDataSize"]
old-location: htmlhelp\iitproplist_getdatasize.htm
tech.root: htmlhelp
ms.assetid: 83d9fa7b-d814-4293-93b9-9454c01c1503
ms.date: 12/05/2018
ms.keywords: GetDataSize, GetDataSize method [HTML Help Workshop], GetDataSize method [HTML Help Workshop],IITPropList interface, IITPropList interface [HTML Help Workshop],GetDataSize method, IITPropList.GetDataSize, IITPropList::GetDataSize, htmlhelp.iitproplist_getdatasize, infotech/IITPropList::GetDataSize
req.header: infotech.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IITPropList::GetDataSize
 - infotech/IITPropList::GetDataSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITPropList.GetDataSize
---

# IITPropList::GetDataSize


## -description

Returns the number of bytes needed to save the property data.

## -parameters

### -param lpvHeader [in]

Pointer to a buffer containing the header.

### -param dwHdrSize [in]

Size of the header buffer.

### -param dwDataSize [out, ref]

Size in bytes.

## -returns

This method can return one of these values.

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
The size was successfully returned. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvHeader</i> parameter is NULL, or <i>dwHdrSize</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BADVALUE</b></dt>
</dl>
</td>
<td width="60%">
Invalid header buffer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitproplist">IITPropList</a>



<a href="/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-getheadersize">IITPropList::GetHeaderSize</a>