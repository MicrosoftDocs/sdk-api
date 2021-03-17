---
UID: NF:infotech.IITPropList.GetHeaderSize
title: IITPropList::GetHeaderSize (infotech.h)
description: Returns the number of bytes needed to save the header.
helpviewer_keywords: ["GetHeaderSize","GetHeaderSize method [HTML Help Workshop]","GetHeaderSize method [HTML Help Workshop]","IITPropList interface","IITPropList interface [HTML Help Workshop]","GetHeaderSize method","IITPropList.GetHeaderSize","IITPropList::GetHeaderSize","htmlhelp.iitproplist_getheadersize","infotech/IITPropList::GetHeaderSize"]
old-location: htmlhelp\iitproplist_getheadersize.htm
tech.root: htmlhelp
ms.assetid: 73206149-cbc3-475d-8dc8-bb7547f41173
ms.date: 12/05/2018
ms.keywords: GetHeaderSize, GetHeaderSize method [HTML Help Workshop], GetHeaderSize method [HTML Help Workshop],IITPropList interface, IITPropList interface [HTML Help Workshop],GetHeaderSize method, IITPropList.GetHeaderSize, IITPropList::GetHeaderSize, htmlhelp.iitproplist_getheadersize, infotech/IITPropList::GetHeaderSize
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
 - IITPropList::GetHeaderSize
 - infotech/IITPropList::GetHeaderSize
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
 - IITPropList.GetHeaderSize
---

# IITPropList::GetHeaderSize


## -description

Returns the number of bytes needed to save the header.

## -parameters

### -param dwHdrSize [out, ref]

Size, in bytes.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitproplist">IITPropList</a>



<a href="/previous-versions/windows/desktop/api/infotech/nf-infotech-iitproplist-getdatasize">IITPropList::GetDataSize</a>