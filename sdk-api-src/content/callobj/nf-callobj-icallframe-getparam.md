---
UID: NF:callobj.ICallFrame.GetParam
title: ICallFrame::GetParam (callobj.h)
description: Retrieves the value of a specified parameter in the call frame.
helpviewer_keywords: ["GetParam","GetParam method [COM]","GetParam method [COM]","ICallFrame interface","ICallFrame interface [COM]","GetParam method","ICallFrame.GetParam","ICallFrame::GetParam","_com_icallframe_getparam","callobj/ICallFrame::GetParam","com.icallframe_getparam"]
old-location: com\icallframe_getparam.htm
tech.root: com
ms.assetid: 43662600-841c-4237-80ac-3822eb47be88
ms.date: 12/05/2018
ms.keywords: GetParam, GetParam method [COM], GetParam method [COM],ICallFrame interface, ICallFrame interface [COM],GetParam method, ICallFrame.GetParam, ICallFrame::GetParam, _com_icallframe_getparam, callobj/ICallFrame::GetParam, com.icallframe_getparam
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
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
 - ICallFrame::GetParam
 - callobj/ICallFrame::GetParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallFrame.GetParam
---

# ICallFrame::GetParam


## -description

Retrieves the value of a specified parameter in the call frame.

## -parameters

### -param iparam [in]

The parameter number.

### -param pvar [out]

The value of the parameter.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>