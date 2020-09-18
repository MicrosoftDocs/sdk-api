---
UID: NF:objidl.IForegroundTransfer.AllowForegroundTransfer
title: IForegroundTransfer::AllowForegroundTransfer (objidl.h)
description: Yields the foreground window to the COM server process.
helpviewer_keywords: ["AllowForegroundTransfer","AllowForegroundTransfer method [COM]","AllowForegroundTransfer method [COM]","IForegroundTransfer interface","IForegroundTransfer interface [COM]","AllowForegroundTransfer method","IForegroundTransfer.AllowForegroundTransfer","IForegroundTransfer::AllowForegroundTransfer","_com_iforegroundtransfer_allowforegroundtransfer","com.iforegroundtransfer_allowforegroundtransfer","objidl/IForegroundTransfer::AllowForegroundTransfer"]
old-location: com\iforegroundtransfer_allowforegroundtransfer.htm
tech.root: com
ms.assetid: 54d138f5-5f16-4eb8-bbac-2d057b7dab2f
ms.date: 12/05/2018
ms.keywords: AllowForegroundTransfer, AllowForegroundTransfer method [COM], AllowForegroundTransfer method [COM],IForegroundTransfer interface, IForegroundTransfer interface [COM],AllowForegroundTransfer method, IForegroundTransfer.AllowForegroundTransfer, IForegroundTransfer::AllowForegroundTransfer, _com_iforegroundtransfer_allowforegroundtransfer, com.iforegroundtransfer_allowforegroundtransfer, objidl/IForegroundTransfer::AllowForegroundTransfer
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IForegroundTransfer::AllowForegroundTransfer
 - objidl/IForegroundTransfer::AllowForegroundTransfer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IForegroundTransfer.AllowForegroundTransfer
---

# IForegroundTransfer::AllowForegroundTransfer


## -description

Yields the foreground window to the COM server process.

## -parameters

### -param lpvReserved [in]

This parameter is reserved and must be <b>NULL</b>.

## -returns

This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvReserved</i> parameter is not <b>NULL</b>, or this interface is on a proxy that does not support foreground control.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-coallowsetforegroundwindow">CoAllowSetForegroundWindow</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iforegroundtransfer">IForegroundTransfer</a>