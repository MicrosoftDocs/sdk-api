---
UID: NF:callobj.ICallIndirect.GetIID
title: ICallIndirect::GetIID (callobj.h)
description: Retrieves the interface id supported by this ICallIndirect implementation.
helpviewer_keywords: ["GetIID","GetIID method [COM]","GetIID method [COM]","ICallIndirect interface","ICallIndirect interface [COM]","GetIID method","ICallIndirect.GetIID","ICallIndirect::GetIID","_com_icallindirect_getiid","callobj/ICallIndirect::GetIID","com.icallindirect_getiid"]
old-location: com\icallindirect_getiid.htm
tech.root: com
ms.assetid: 096bd49e-2fad-4558-98c7-c95e0dc43a65
ms.date: 12/05/2018
ms.keywords: GetIID, GetIID method [COM], GetIID method [COM],ICallIndirect interface, ICallIndirect interface [COM],GetIID method, ICallIndirect.GetIID, ICallIndirect::GetIID, _com_icallindirect_getiid, callobj/ICallIndirect::GetIID, com.icallindirect_getiid
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
 - ICallIndirect::GetIID
 - callobj/ICallIndirect::GetIID
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
 - ICallIndirect.GetIID
---

# ICallIndirect::GetIID


## -description

Retrieves the interface id supported by this <a href="/windows/desktop/api/callobj/nn-callobj-icallindirect">ICallIndirect</a> implementation.

## -parameters

### -param piid [out]

A pointer to the interface. This parameter is optional.

### -param pfDerivesFromIDispatch [out]

Indicates whether the interface is derived from <b>IDispatch</b>. This parameter is optional.

### -param pcMethod [out]

Receives the number of methods in the interface.

### -param pwszInterface [out]

Receives the interface name if it is available.

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

<a href="/windows/desktop/api/callobj/nn-callobj-icallindirect">ICallIndirect</a>