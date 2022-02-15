---
UID: NF:wmcodecdsp.ITocParser.GetTocByType
title: ITocParser::GetTocByType (wmcodecdsp.h)
description: The GetTocByType retrieves all tables of contents of a specified type from the TOC Parser object.
helpviewer_keywords: ["GetTocByType","GetTocByType method [Media Foundation]","GetTocByType method [Media Foundation]","ITocParser interface","ITocParser interface [Media Foundation]","GetTocByType method","ITocParser.GetTocByType","ITocParser::GetTocByType","codecapi.itocparser_gettocbytype","mf.itocparser_gettocbytype","wmcodecdsp/ITocParser::GetTocByType"]
old-location: mf\itocparser_gettocbytype.htm
tech.root: mf
ms.assetid: 97a3b835-5d99-4b37-8f1d-2469e85faf9b
ms.date: 12/05/2018
ms.keywords: GetTocByType, GetTocByType method [Media Foundation], GetTocByType method [Media Foundation],ITocParser interface, ITocParser interface [Media Foundation],GetTocByType method, ITocParser.GetTocByType, ITocParser::GetTocByType, codecapi.itocparser_gettocbytype, mf.itocparser_gettocbytype, wmcodecdsp/ITocParser::GetTocByType
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
 - ITocParser::GetTocByType
 - wmcodecdsp/ITocParser::GetTocByType
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
 - ITocParser.GetTocByType
---

# ITocParser::GetTocByType


## -description

The <b>GetTocByType</b> retrieves all tables of contents of a specified type from the TOC Parser object.

## -parameters

### -param unnamedParam1 [in]

A member of the <a href="/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type">TOC_POS_TYPE</a> enumeration that specifies the <a href="/windows/desktop/medfound/the-position-type-of-a-table-of-contents">position type</a> of the table of contents to be retrieved.

### -param guidTocType [in]

A globally unique identifier (<b>GUID</b>) that specifies the type of table of contents to retrieve. See Remarks.

### -param ppTocs [out]

Pointer to an <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoccollection">ITocCollection</a> interface that represents the collection of retrieved tables of contents.

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

## -remarks

You might want to design several different type of tables of contents. In that case, you can distinguish between types by creating a <b>GUID</b> that represents each type. You can identify a table of contents as a particular type by setting the <b>guidType</b> member of a <a href="/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_descriptor">TOC_DESCRIPTOR</a> structure and then passing the <b>TOC_DESCRIPTOR</b> structure to <a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setdescriptor">IToc::SetDescriptor</a>.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser">ITocParser</a>



<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype">RemoveTocByType</a>