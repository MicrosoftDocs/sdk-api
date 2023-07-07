---
UID: NF:sbe.IStreamBufferConfigure.GetDirectory
title: IStreamBufferConfigure::GetDirectory (sbe.h)
description: The GetDirectory method retrieves the directory where backing files are saved.
helpviewer_keywords: ["GetDirectory","GetDirectory method [Microsoft TV Technologies]","GetDirectory method [Microsoft TV Technologies]","IStreamBufferConfigure interface","IStreamBufferConfigure interface [Microsoft TV Technologies]","GetDirectory method","IStreamBufferConfigure.GetDirectory","IStreamBufferConfigure::GetDirectory","IStreamBufferConfigureGetDirectory","mstv.istreambufferconfigure_getdirectory","sbe/IStreamBufferConfigure::GetDirectory"]
old-location: mstv\istreambufferconfigure_getdirectory.htm
tech.root: mstv
ms.assetid: bb5d955d-11da-4ff3-990f-02c0c80d6405
ms.date: 12/05/2018
ms.keywords: GetDirectory, GetDirectory method [Microsoft TV Technologies], GetDirectory method [Microsoft TV Technologies],IStreamBufferConfigure interface, IStreamBufferConfigure interface [Microsoft TV Technologies],GetDirectory method, IStreamBufferConfigure.GetDirectory, IStreamBufferConfigure::GetDirectory, IStreamBufferConfigureGetDirectory, mstv.istreambufferconfigure_getdirectory, sbe/IStreamBufferConfigure::GetDirectory
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IStreamBufferConfigure::GetDirectory
 - sbe/IStreamBufferConfigure::GetDirectory
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
 - IStreamBufferConfigure.GetDirectory
---

# IStreamBufferConfigure::GetDirectory


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetDirectory</b> method retrieves the directory where backing files are saved.

## -parameters

### -param ppszDirectoryName [out]

Pointer to a variable that receives the fully qualified directory name.

## -returns

Returns an <b>HRESULT</b>. Possible values include those in the following table.

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

The caller must free the returned string by calling <b>CoTaskMemFree</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure">IStreamBufferConfigure Interface</a>