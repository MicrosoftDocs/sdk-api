---
UID: NF:callobj.ICallFrame.GetParamInfo
title: ICallFrame::GetParamInfo (callobj.h)
description: Retrieves the information for the specified parameter.
helpviewer_keywords: ["GetParamInfo","GetParamInfo method [COM]","GetParamInfo method [COM]","ICallFrame interface","ICallFrame interface [COM]","GetParamInfo method","ICallFrame.GetParamInfo","ICallFrame::GetParamInfo","_com_icallframe_getparaminfo","callobj/ICallFrame::GetParamInfo","com.icallframe_getparaminfo"]
old-location: com\icallframe_getparaminfo.htm
tech.root: com
ms.assetid: fb75930d-8e1b-4e97-87f2-bb9d171658a8
ms.date: 12/05/2018
ms.keywords: GetParamInfo, GetParamInfo method [COM], GetParamInfo method [COM],ICallFrame interface, ICallFrame interface [COM],GetParamInfo method, ICallFrame.GetParamInfo, ICallFrame::GetParamInfo, _com_icallframe_getparaminfo, callobj/ICallFrame::GetParamInfo, com.icallframe_getparaminfo
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
 - ICallFrame::GetParamInfo
 - callobj/ICallFrame::GetParamInfo
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
 - ICallFrame.GetParamInfo
---

# ICallFrame::GetParamInfo


## -description

Retrieves the information for the specified parameter.

## -parameters

### -param iparam [in]

The parameter number.

### -param pInfo [out]

A pointer to a <a href="/windows/win32/api/callobj/ns-callobj-callframeparaminfo">CALLFRAMEPARAMINFO</a> structure.

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