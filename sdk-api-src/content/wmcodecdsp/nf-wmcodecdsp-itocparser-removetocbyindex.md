---
UID: NF:wmcodecdsp.ITocParser.RemoveTocByIndex
title: ITocParser::RemoveTocByIndex (wmcodecdsp.h)
description: The RemoveTocByIndex method removes a table of contents, specified by an index, from the TOC Parser object.
helpviewer_keywords: ["ITocParser interface [Media Foundation]","RemoveTocByIndex method","ITocParser.RemoveTocByIndex","ITocParser::RemoveTocByIndex","RemoveTocByIndex","RemoveTocByIndex method [Media Foundation]","RemoveTocByIndex method [Media Foundation]","ITocParser interface","codecapi.itocparser_removetocbyindex","mf.itocparser_removetocbyindex","wmcodecdsp/ITocParser::RemoveTocByIndex"]
old-location: mf\itocparser_removetocbyindex.htm
tech.root: medfound
ms.assetid: 7ec459bf-c631-4ad4-beb3-4cd1e89c1d35
ms.date: 12/05/2018
ms.keywords: ITocParser interface [Media Foundation],RemoveTocByIndex method, ITocParser.RemoveTocByIndex, ITocParser::RemoveTocByIndex, RemoveTocByIndex, RemoveTocByIndex method [Media Foundation], RemoveTocByIndex method [Media Foundation],ITocParser interface, codecapi.itocparser_removetocbyindex, mf.itocparser_removetocbyindex, wmcodecdsp/ITocParser::RemoveTocByIndex
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Wmvdspa.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITocParser::RemoveTocByIndex
 - wmcodecdsp/ITocParser::RemoveTocByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - ITocParser.RemoveTocByIndex
---

# ITocParser::RemoveTocByIndex


## -description

The <b>RemoveTocByIndex</b> method removes a table of contents, specified by an index, from the TOC Parser object.

## -parameters

### -param unnamedParam1 [in]

A member of the <a href="/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type">TOC_POS_TYPE</a> enumeration that specifies the <a href="/windows/desktop/medfound/the-position-type-of-a-table-of-contents">position type</a> of the table of contents to be removed.

### -param dwTocIndex [in]

The index of the table of contents to be removed.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser">ITocParser</a>