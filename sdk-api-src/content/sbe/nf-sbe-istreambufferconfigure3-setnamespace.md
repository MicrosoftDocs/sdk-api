---
UID: NF:sbe.IStreamBufferConfigure3.SetNamespace
title: IStreamBufferConfigure3::SetNamespace (sbe.h)
description: The SetNamespace method specifies a prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.
helpviewer_keywords: ["IStreamBufferConfigure3 interface [Microsoft TV Technologies]","SetNamespace method","IStreamBufferConfigure3.SetNamespace","IStreamBufferConfigure3::SetNamespace","IStreamBufferConfigure3SetNamespace","SetNamespace","SetNamespace method [Microsoft TV Technologies]","SetNamespace method [Microsoft TV Technologies]","IStreamBufferConfigure3 interface","mstv.istreambufferconfigure3_setnamespace","sbe/IStreamBufferConfigure3::SetNamespace"]
old-location: mstv\istreambufferconfigure3_setnamespace.htm
tech.root: mstv
ms.assetid: e009e078-99f5-4da1-88ce-c07e9588c5e8
ms.date: 12/05/2018
ms.keywords: IStreamBufferConfigure3 interface [Microsoft TV Technologies],SetNamespace method, IStreamBufferConfigure3.SetNamespace, IStreamBufferConfigure3::SetNamespace, IStreamBufferConfigure3SetNamespace, SetNamespace, SetNamespace method [Microsoft TV Technologies], SetNamespace method [Microsoft TV Technologies],IStreamBufferConfigure3 interface, mstv.istreambufferconfigure3_setnamespace, sbe/IStreamBufferConfigure3::SetNamespace
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferConfigure3::SetNamespace
 - sbe/IStreamBufferConfigure3::SetNamespace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure3.SetNamespace
---

# IStreamBufferConfigure3::SetNamespace


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetNamespace</b> method specifies a prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.

## -parameters

### -param pszNamespace [in]

Pointer to a null-terminated wide character string. If <b>NULL</b>, no prefix is used. Currently, the following values are supported.

<ul>
<li>L"Global"</li>
<li><b>NULL</b></li>
</ul>

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
<dt><b>CO_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The specified prefix is not supported.

</td>
</tr>
</table>

## -remarks

The default value is "Global".

If the value is "Global", the synchronization objects are created in the global name space, which requires administrator privileges in Windows Vista or later. If the value is <b>NULL</b>, the synchronization objects are created in the local session name space, which does not require administrator privileges.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure3">IStreamBufferConfigure3 Interface</a>