---
UID: NF:wmcodecdsp.ITocParser.AddToc
title: ITocParser::AddToc (wmcodecdsp.h)
description: The AddToc method adds a table of contents to the TOC Parser object and assigns an index to the added table of contents.
helpviewer_keywords: ["AddToc","AddToc method [Media Foundation]","AddToc method [Media Foundation]","ITocParser interface","ITocParser interface [Media Foundation]","AddToc method","ITocParser.AddToc","ITocParser::AddToc","codecapi.itocparser_addtoc","mf.itocparser_addtoc","wmcodecdsp/ITocParser::AddToc"]
old-location: mf\itocparser_addtoc.htm
tech.root: mf
ms.assetid: c99ccbb3-ba33-4d87-81a3-0de3c180554a
ms.date: 12/05/2018
ms.keywords: AddToc, AddToc method [Media Foundation], AddToc method [Media Foundation],ITocParser interface, ITocParser interface [Media Foundation],AddToc method, ITocParser.AddToc, ITocParser::AddToc, codecapi.itocparser_addtoc, mf.itocparser_addtoc, wmcodecdsp/ITocParser::AddToc
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
 - ITocParser::AddToc
 - wmcodecdsp/ITocParser::AddToc
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
 - ITocParser.AddToc
---

# ITocParser::AddToc


## -description

The <b>AddToc</b> method adds a table of contents to the TOC Parser object and assigns an index to the added table of contents.

## -parameters

### -param unnamedParam1 [in]

A member of the <a href="/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type">TOC_POS_TYPE</a> enumeration that specifies the <a href="/windows/desktop/medfound/the-position-type-of-a-table-of-contents">position type</a> of the table of contents to be added.

### -param pToc [in]

Pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc">IToc</a> interface that represents the table of contents to be added.

### -param pdwTocIndex [out]

Pointer to a <b>DWORD</b> that receives the index of the added table of contents.

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

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex">GetTocByIndex</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser">ITocParser</a>