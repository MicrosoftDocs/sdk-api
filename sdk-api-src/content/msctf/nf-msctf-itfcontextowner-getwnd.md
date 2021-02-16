---
UID: NF:msctf.ITfContextOwner.GetWnd
title: ITfContextOwner::GetWnd (msctf.h)
description: The ITfContextOwner::GetWnd method returns the handle to a window that corresponds to the current document.
helpviewer_keywords: ["GetWnd","GetWnd method [Text Services Framework]","GetWnd method [Text Services Framework]","ITfContextOwner interface","ITfContextOwner interface [Text Services Framework]","GetWnd method","ITfContextOwner.GetWnd","ITfContextOwner::GetWnd","_tsf_itfcontextowner_getwnd_ref","msctf/ITfContextOwner::GetWnd","tsf.itfcontextowner_getwnd"]
old-location: tsf\itfcontextowner_getwnd.htm
tech.root: TSF
ms.assetid: 91dfc873-3327-49f4-924a-b013fa90459b
ms.date: 12/05/2018
ms.keywords: GetWnd, GetWnd method [Text Services Framework], GetWnd method [Text Services Framework],ITfContextOwner interface, ITfContextOwner interface [Text Services Framework],GetWnd method, ITfContextOwner.GetWnd, ITfContextOwner::GetWnd, _tsf_itfcontextowner_getwnd_ref, msctf/ITfContextOwner::GetWnd, tsf.itfcontextowner_getwnd
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msimtf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwner::GetWnd
 - msctf/ITfContextOwner::GetWnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwner.GetWnd
---

# ITfContextOwner::GetWnd


## -description

The <b>ITfContextOwner::GetWnd</b> method returns the handle to a window that corresponds to the current document.

## -parameters

### -param phwnd [out]

Receives a pointer to the handle of the window that corresponds to the current document. This parameter can be <b>NULL</b> if the document does not have the corresponding handle to the window.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -remarks

A document might not have a corresponding window handle if the document is in memory but not displayed on the screen or if the document is a windowless control and the control does not know the window handle of the owner of the windowless controls. Callers cannot assume that the <i>phwnd</i> parameter will receive a non-<b>NULL</b> value even if the method is successful. Callers can also receive a <b>NULL</b> value for the <i>phwnd</i> parameter.

