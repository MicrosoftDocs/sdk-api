---
UID: NF:wmcontainer.IMFASFSplitter.SetFlags
title: IMFASFSplitter::SetFlags (wmcontainer.h)
description: Sets option flags on the Advanced Systems Format (ASF) splitter.
helpviewer_keywords: ["5c70e5a0-7dd5-49c5-af35-4d9568871b41","IMFASFSplitter interface [Media Foundation]","SetFlags method","IMFASFSplitter.SetFlags","IMFASFSplitter::SetFlags","SetFlags","SetFlags method [Media Foundation]","SetFlags method [Media Foundation]","IMFASFSplitter interface","mf.imfasfsplitter_setflags","wmcontainer/IMFASFSplitter::SetFlags"]
old-location: mf\imfasfsplitter_setflags.htm
tech.root: mf
ms.assetid: 5c70e5a0-7dd5-49c5-af35-4d9568871b41
ms.date: 12/05/2018
ms.keywords: 5c70e5a0-7dd5-49c5-af35-4d9568871b41, IMFASFSplitter interface [Media Foundation],SetFlags method, IMFASFSplitter.SetFlags, IMFASFSplitter::SetFlags, SetFlags, SetFlags method [Media Foundation], SetFlags method [Media Foundation],IMFASFSplitter interface, mf.imfasfsplitter_setflags, wmcontainer/IMFASFSplitter::SetFlags
req.header: wmcontainer.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFSplitter::SetFlags
 - wmcontainer/IMFASFSplitter::SetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFSplitter.SetFlags
---

# IMFASFSplitter::SetFlags


## -description

Sets option flags on the Advanced Systems Format (ASF) splitter.

## -parameters

### -param dwFlags [in]

A bitwise combination of zero or more members of the <a href="/windows/desktop/api/wmcontainer/ne-wmcontainer-mfasf_splitterflags">MFASF_SPLITTERFLAGS</a> enumeration.

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
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The splitter is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter does not contain a valid flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The MFASF_SPLITTER_REVERSE flag is set, but the content cannot be parsed in reverse.

</td>
</tr>
</table>

## -remarks

This method can only be called after the splitter is initialized.

## -see-also

<a href="/windows/desktop/medfound/asf-splitter">ASF Splitter</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter">IMFASFSplitter</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags">IMFASFSplitter::GetFlags</a>