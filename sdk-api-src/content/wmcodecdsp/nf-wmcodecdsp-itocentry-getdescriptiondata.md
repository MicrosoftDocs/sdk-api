---
UID: NF:wmcodecdsp.ITocEntry.GetDescriptionData
title: ITocEntry::GetDescriptionData (wmcodecdsp.h)
description: The GetDescriptionData method gets a description data block that was previously associated with the entry by a call to SetDescriptionData.
helpviewer_keywords: ["GetDescriptionData","GetDescriptionData method [Media Foundation]","GetDescriptionData method [Media Foundation]","ITocEntry interface","ITocEntry interface [Media Foundation]","GetDescriptionData method","ITocEntry.GetDescriptionData","ITocEntry::GetDescriptionData","codecapi.itocentry_getdescriptiondata","mf.itocentry_getdescriptiondata","wmcodecdsp/ITocEntry::GetDescriptionData"]
old-location: mf\itocentry_getdescriptiondata.htm
tech.root: mf
ms.assetid: 4000b67c-e34e-4bce-9a0d-c56c9fc0f41e
ms.date: 12/05/2018
ms.keywords: GetDescriptionData, GetDescriptionData method [Media Foundation], GetDescriptionData method [Media Foundation],ITocEntry interface, ITocEntry interface [Media Foundation],GetDescriptionData method, ITocEntry.GetDescriptionData, ITocEntry::GetDescriptionData, codecapi.itocentry_getdescriptiondata, mf.itocentry_getdescriptiondata, wmcodecdsp/ITocEntry::GetDescriptionData
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
 - ITocEntry::GetDescriptionData
 - wmcodecdsp/ITocEntry::GetDescriptionData
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
 - ITocEntry.GetDescriptionData
---

# ITocEntry::GetDescriptionData


## -description

The <b>GetDescriptionData</b> method gets a description data block that was previously associated with the entry by a call to <a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptiondata">SetDescriptionData</a>.

## -parameters

### -param pdwDescriptionDataSize [in, out]

If <i>pbtDescriptionData</i> is <b>NULL</b>, this is an output parameter that receives the size, in bytes, of the description data block. If <i>pbtDescriptionData</i> is not <b>NULL</b>, this is an input parameter that specifies the size, in bytes, of the caller-allocated buffer pointed to by <i>pbtDescriptionData</i>.

### -param pbtDescriptionData [out]

NULL, or a pointer to a caller-allocated buffer that, on successful completion, receives the description data block.

### -param pGuidType [out]

Pointer to a variable that receives a globally unique identifier (GUID) that identifies the type of data in the description data block. See Remarks.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The method returns this error code if <i>pbtDescriptionData</i> is not <b>NULL</b> and the context block is larger than the size specified by <i>pdwDescriptionDataSize</i>. In that case, <i>pdwDescriptionDataSize</i> serves as an output parameter and receives the size, in bytes, of the required buffer.

</td>
</tr>
</table>

## -remarks

You can associate only one description data block with a given entry at a given time. However, you might want to design different types of description data blocks and identify each type of block with a globally unique identifier (GUID). That way, when you call <a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptiondata">SetDescriptionData</a>, you can mark the data block as being of a specific type. When you call <b>GetDescriptionData</b>, you can determine the type of the data block retrieved by inspecting the value returned in <i>pGuidType</i>.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry">ITocEntry</a>



<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptiondata">SetDescriptionData</a>