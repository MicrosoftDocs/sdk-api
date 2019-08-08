---
UID: NF:wmcodecdsp.ITocParser.RemoveTocByType
title: ITocParser::RemoveTocByType (wmcodecdsp.h)
author: windows-sdk-content
description: The RemoveTocByType method removes all tables of contents of a specified type from the TOC Parser object.
old-location: mf\itocparser_removetocbytype.htm
tech.root: medfound
ms.assetid: e3d32dc9-ccae-46fd-9dd4-62e300981da0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITocParser interface [Media Foundation],RemoveTocByType method, ITocParser.RemoveTocByType, ITocParser::RemoveTocByType, RemoveTocByType, RemoveTocByType method [Media Foundation], RemoveTocByType method [Media Foundation],ITocParser interface, codecapi.itocparser_removetocbytype, mf.itocparser_removetocbytype, wmcodecdsp/ITocParser::RemoveTocByType
ms.topic: method
f1_keywords:
- wmcodecdsp/ITocParser.RemoveTocByType
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmvdspa.dll
api_name:
- ITocParser.RemoveTocByType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITocParser::RemoveTocByType


## -description


The <b>RemoveTocByType</b> method removes all tables of contents of a specified type from the TOC Parser object.


## -parameters




### -param arg1 [in]

A member of the <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type">TOC_POS_TYPE</a> enumeration that specifies the <a href="https://docs.microsoft.com/windows/desktop/medfound/the-position-type-of-a-table-of-contents">position type</a> of the tables of contents to be removed.


### -param guidTocType [in]

A globally unique identifier (<b>GUID</b>) that specifies the type of table of contents to removed. See Remarks.


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



You might want to design several different type of tables of contents. In that case, you can distinguish between types by creating a <b>GUID</b> that represents each type. You can identify a table of contents as a particular type by setting the <b>guidType</b> member of a <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_descriptor">TOC_DESCRIPTOR</a> structure and then passing the <b>TOC_DESCRIPTOR</b> structure to <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setdescriptor">IToc::SetDescriptor</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser">ITocParser</a>
 

 

