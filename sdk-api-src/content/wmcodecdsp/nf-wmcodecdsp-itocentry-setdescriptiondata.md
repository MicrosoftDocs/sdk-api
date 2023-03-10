---
UID: NF:wmcodecdsp.ITocEntry.SetDescriptionData
title: ITocEntry::SetDescriptionData (wmcodecdsp.h)
description: The SetDescriptionData method associates a caller-supplied data block with the entry.
helpviewer_keywords: ["ITocEntry interface [Media Foundation]","SetDescriptionData method","ITocEntry.SetDescriptionData","ITocEntry::SetDescriptionData","SetDescriptionData","SetDescriptionData method [Media Foundation]","SetDescriptionData method [Media Foundation]","ITocEntry interface","codecapi.itocentry_setdescriptiondata","mf.itocentry_setdescriptiondata","wmcodecdsp/ITocEntry::SetDescriptionData"]
old-location: mf\itocentry_setdescriptiondata.htm
tech.root: mf
ms.assetid: 260d7699-cf75-4179-9f2b-bc3bc49c94e6
ms.date: 12/05/2018
ms.keywords: ITocEntry interface [Media Foundation],SetDescriptionData method, ITocEntry.SetDescriptionData, ITocEntry::SetDescriptionData, SetDescriptionData, SetDescriptionData method [Media Foundation], SetDescriptionData method [Media Foundation],ITocEntry interface, codecapi.itocentry_setdescriptiondata, mf.itocentry_setdescriptiondata, wmcodecdsp/ITocEntry::SetDescriptionData
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
 - ITocEntry::SetDescriptionData
 - wmcodecdsp/ITocEntry::SetDescriptionData
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
 - ITocEntry.SetDescriptionData
---

# ITocEntry::SetDescriptionData


## -description

The <b>SetDescriptionData</b> method associates a caller-supplied data block with the entry.

## -parameters

### -param dwDescriptionDataSize [in]

The size, in bytes, of the data block.

### -param pbtDescriptionData [in]

Pointer to the first byte of the data block.

### -param pguidType [in]

Pointer to a <b>GUID</b> that identifies the type of data in the block. This parameter can be <b>NULL</b>. See Remarks.

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

You can use this method to associate any information of your choice with the entry. The nature of the information you store in the description data block is completely up to you. TOC Parser does not inspect or interpret the description data block.

You can associate only one description data block with a given entry at a given time. However, you might want to design different types of description data blocks and identify each type of block with a globally unique identifier (GUID). That way, you could associate description data of a certain type with some of your entries and description data of a different type with other entries. If you do not need to distinguish between different types of description data blocks, you can set <i>pguidType</i> to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptiondata">GetDescriptionData</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry">ITocEntry</a>