---
UID: NF:wmcodecdsp.ITocParser.GetTocByIndex
title: ITocParser::GetTocByIndex (wmcodecdsp.h)
description: The GetTocByIndex method retrieves a table of contents, specified by an index, from the TOC Parser object.
helpviewer_keywords: ["GetTocByIndex","GetTocByIndex method [Media Foundation]","GetTocByIndex method [Media Foundation]","ITocParser interface","ITocParser interface [Media Foundation]","GetTocByIndex method","ITocParser.GetTocByIndex","ITocParser::GetTocByIndex","codecapi.itocparser_gettocbyindex","mf.itocparser_gettocbyindex","wmcodecdsp/ITocParser::GetTocByIndex"]
old-location: mf\itocparser_gettocbyindex.htm
tech.root: medfound
ms.assetid: 1386e348-c94f-4343-908c-338352eae494
ms.date: 12/05/2018
ms.keywords: GetTocByIndex, GetTocByIndex method [Media Foundation], GetTocByIndex method [Media Foundation],ITocParser interface, ITocParser interface [Media Foundation],GetTocByIndex method, ITocParser.GetTocByIndex, ITocParser::GetTocByIndex, codecapi.itocparser_gettocbyindex, mf.itocparser_gettocbyindex, wmcodecdsp/ITocParser::GetTocByIndex
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
 - ITocParser::GetTocByIndex
 - wmcodecdsp/ITocParser::GetTocByIndex
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
 - ITocParser.GetTocByIndex
---

# ITocParser::GetTocByIndex


## -description

The <b>GetTocByIndex</b> method retrieves a table of contents, specified by an index, from the TOC Parser object.

## -parameters

### -param unnamedParam1 [in]

A member of the <a href="/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type">TOC_POS_TYPE</a> enumeration that specifies the <a href="/windows/desktop/medfound/the-position-type-of-a-table-of-contents">position type</a> of the table of contents to be retrieved.

### -param dwTocIndex [in]

The index of the table of contents to be retrieved.

### -param ppToc [out]

Pointer to a variable that receives a pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a> interface that represents the retrieved table of contents.

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

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser">ITocParser Interface</a>