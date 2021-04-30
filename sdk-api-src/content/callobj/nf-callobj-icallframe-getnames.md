---
UID: NF:callobj.ICallFrame.GetNames
title: ICallFrame::GetNames (callobj.h)
description: Retrieves the method or interface name of this call.
helpviewer_keywords: ["GetNames","GetNames method [COM]","GetNames method [COM]","ICallFrame interface","ICallFrame interface [COM]","GetNames method","ICallFrame.GetNames","ICallFrame::GetNames","_com_icallframe_getnames","callobj/ICallFrame::GetNames","com.icallframe_getnames"]
old-location: com\icallframe_getnames.htm
tech.root: com
ms.assetid: 3efb0819-51db-419b-a9f1-710bb3abae2d
ms.date: 12/05/2018
ms.keywords: GetNames, GetNames method [COM], GetNames method [COM],ICallFrame interface, ICallFrame interface [COM],GetNames method, ICallFrame.GetNames, ICallFrame::GetNames, _com_icallframe_getnames, callobj/ICallFrame::GetNames, com.icallframe_getnames
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
 - ICallFrame::GetNames
 - callobj/ICallFrame::GetNames
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
 - ICallFrame.GetNames
---

# ICallFrame::GetNames


## -description

Retrieves the method or interface name of this call.

## -parameters

### -param pwszInterface [out]

A pointer to the interface name.

### -param pwszMethod [out]

A pointer to the method name.

## -returns

If the requested name is not available, the return value is a null string. This method can also return the following values.

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