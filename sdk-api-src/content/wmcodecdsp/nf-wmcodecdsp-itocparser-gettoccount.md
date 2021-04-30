---
UID: NF:wmcodecdsp.ITocParser.GetTocCount
title: ITocParser::GetTocCount (wmcodecdsp.h)
description: The GetTocCount method retrieves the number of tables of contents, of a specified position type, in the TOC Parser object.
helpviewer_keywords: ["GetTocCount","GetTocCount method [Media Foundation]","GetTocCount method [Media Foundation]","ITocParser interface","ITocParser interface [Media Foundation]","GetTocCount method","ITocParser.GetTocCount","ITocParser::GetTocCount","codecapi.itocparser_gettoccount","mf.itocparser_gettoccount","wmcodecdsp/ITocParser::GetTocCount"]
old-location: mf\itocparser_gettoccount.htm
tech.root: mf
ms.assetid: 8ad80a20-cadb-4a0d-a39e-b627324df425
ms.date: 12/05/2018
ms.keywords: GetTocCount, GetTocCount method [Media Foundation], GetTocCount method [Media Foundation],ITocParser interface, ITocParser interface [Media Foundation],GetTocCount method, ITocParser.GetTocCount, ITocParser::GetTocCount, codecapi.itocparser_gettoccount, mf.itocparser_gettoccount, wmcodecdsp/ITocParser::GetTocCount
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
 - ITocParser::GetTocCount
 - wmcodecdsp/ITocParser::GetTocCount
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
 - ITocParser.GetTocCount
---

# ITocParser::GetTocCount


## -description

The <b>GetTocCount</b> method retrieves the number of tables of contents, of a specified <a href="/windows/desktop/medfound/the-position-type-of-a-table-of-contents">position type</a>, in the TOC Parser object.

## -parameters

### -param unnamedParam1 [in]

A member of the <a href="/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type">TOC_POS_TYPE</a> enumeration that specifies the <a href="/windows/desktop/medfound/the-position-type-of-a-table-of-contents">position type</a> of the tables of contents to be counted.

### -param pdwTocCount [out]

Pointer to a <b>DWORD</b> that receives the number of tables of contents.

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