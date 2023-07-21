---
UID: NF:sbe.IStreamBufferConfigure3.GetNamespace
title: IStreamBufferConfigure3::GetNamespace (sbe.h)
description: The GetNamespace method retrieves the prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.
helpviewer_keywords: ["GetNamespace","GetNamespace method [Microsoft TV Technologies]","GetNamespace method [Microsoft TV Technologies]","IStreamBufferConfigure3 interface","IStreamBufferConfigure3 interface [Microsoft TV Technologies]","GetNamespace method","IStreamBufferConfigure3.GetNamespace","IStreamBufferConfigure3::GetNamespace","IStreamBufferConfigure3GetNamespace","mstv.istreambufferconfigure3_getnamespace","sbe/IStreamBufferConfigure3::GetNamespace"]
old-location: mstv\istreambufferconfigure3_getnamespace.htm
tech.root: mstv
ms.assetid: c03b5edd-e2b2-4ac9-b2e7-080f3796a6cc
ms.date: 12/05/2018
ms.keywords: GetNamespace, GetNamespace method [Microsoft TV Technologies], GetNamespace method [Microsoft TV Technologies],IStreamBufferConfigure3 interface, IStreamBufferConfigure3 interface [Microsoft TV Technologies],GetNamespace method, IStreamBufferConfigure3.GetNamespace, IStreamBufferConfigure3::GetNamespace, IStreamBufferConfigure3GetNamespace, mstv.istreambufferconfigure3_getnamespace, sbe/IStreamBufferConfigure3::GetNamespace
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
 - IStreamBufferConfigure3::GetNamespace
 - sbe/IStreamBufferConfigure3::GetNamespace
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
 - IStreamBufferConfigure3.GetNamespace
---

# IStreamBufferConfigure3::GetNamespace


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetNamespace</b> method retrieves the prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.

## -parameters

### -param ppszNamespace [out]

Receives a pointer to a null-terminated, wide-character string. The caller must free the string by calling <b>CoTaskMemFree</b>. If no prefix is defined, this variable receives a <b>NULL</b> pointer.

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

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure3">IStreamBufferConfigure3 Interface</a>