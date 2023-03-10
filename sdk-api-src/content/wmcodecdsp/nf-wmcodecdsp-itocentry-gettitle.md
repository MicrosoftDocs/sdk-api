---
UID: NF:wmcodecdsp.ITocEntry.GetTitle
title: ITocEntry::GetTitle (wmcodecdsp.h)
description: The GetTitle method retrieves the title, set by a previous call to SetTitle, of the entry.
helpviewer_keywords: ["GetTitle","GetTitle method [Media Foundation]","GetTitle method [Media Foundation]","ITocEntry interface","ITocEntry interface [Media Foundation]","GetTitle method","ITocEntry.GetTitle","ITocEntry::GetTitle","codecapi.itocentry_gettitle","mf.itocentry_gettitle","wmcodecdsp/ITocEntry::GetTitle"]
old-location: mf\itocentry_gettitle.htm
tech.root: mf
ms.assetid: d610e9e8-daa4-4d8c-a640-627b23afd316
ms.date: 12/05/2018
ms.keywords: GetTitle, GetTitle method [Media Foundation], GetTitle method [Media Foundation],ITocEntry interface, ITocEntry interface [Media Foundation],GetTitle method, ITocEntry.GetTitle, ITocEntry::GetTitle, codecapi.itocentry_gettitle, mf.itocentry_gettitle, wmcodecdsp/ITocEntry::GetTitle
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
 - ITocEntry::GetTitle
 - wmcodecdsp/ITocEntry::GetTitle
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
 - ITocEntry.GetTitle
---

# ITocEntry::GetTitle


## -description

The <b>GetTitle</b> method retrieves the title, set by a previous call to <a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-settitle">SetTitle</a>, of the entry.

## -parameters

### -param pwTitleSize [in, out]

If <i>pwszTitle</i> is <b>NULL</b>, this is an output parameter that receives the size, in wide characters, of the buffer required to receive the title. If <i>pwszTitle</i> is not <b>NULL</b>, this is an input parameter that specifies the size, in wide characters, of the caller-allocated buffer pointed to by <i>pwszTitle</i>.

### -param pwszTitle [out]

<b>NULL</b>, or a pointer to a caller-allocated buffer that, on successful completion, receives the title. The title  is null-terminated.

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
The method returns this error code if <i>pwszTitle</i> is not <b>NULL</b> and the title, including its NULL terminator, is larger than the size specified by <i>pwTitleSize</i>. In that case, <i>pwTitleSize</i> serves as an output parameter and receives the size of the required buffer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry">ITocEntry</a>



<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-settitle">SetTitle</a>