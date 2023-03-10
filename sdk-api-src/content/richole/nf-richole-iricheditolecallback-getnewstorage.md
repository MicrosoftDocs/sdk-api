---
UID: NF:richole.IRichEditOleCallback.GetNewStorage
title: IRichEditOleCallback::GetNewStorage (richole.h)
description: Provides storage for a new object pasted from the clipboard or read in from an Rich Text Format (RTF) stream.
helpviewer_keywords: ["GetNewStorage","GetNewStorage method [Windows Controls]","GetNewStorage method [Windows Controls]","IRichEditOleCallback interface","IRichEditOleCallback interface [Windows Controls]","GetNewStorage method","IRichEditOleCallback.GetNewStorage","IRichEditOleCallback::GetNewStorage","_win32_IRichEditOleCallback_GetNewStorage","_win32_IRichEditOleCallback_GetNewStorage_cpp","controls.IRichEditOleCallback_GetNewStorage","controls._win32_IRichEditOleCallback_GetNewStorage","richole/IRichEditOleCallback::GetNewStorage"]
old-location: controls\IRichEditOleCallback_GetNewStorage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackgetnewstorage.htm
ms.date: 12/05/2018
ms.keywords: GetNewStorage, GetNewStorage method [Windows Controls], GetNewStorage method [Windows Controls],IRichEditOleCallback interface, IRichEditOleCallback interface [Windows Controls],GetNewStorage method, IRichEditOleCallback.GetNewStorage, IRichEditOleCallback::GetNewStorage, _win32_IRichEditOleCallback_GetNewStorage, _win32_IRichEditOleCallback_GetNewStorage_cpp, controls.IRichEditOleCallback_GetNewStorage, controls._win32_IRichEditOleCallback_GetNewStorage, richole/IRichEditOleCallback::GetNewStorage
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRichEditOleCallback::GetNewStorage
 - richole/IRichEditOleCallback::GetNewStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOleCallback.GetNewStorage
---

# IRichEditOleCallback::GetNewStorage


## -description

Provides storage for a new object pasted from the clipboard or read in from an Rich Text Format (RTF) stream.

## -parameters

### -param lplpstg

Type: <b>LPSTORAGE*</b>

The address of the <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface created for the new object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b> on success. If the method fails, it can return one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
There was an invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory to do the operation.

</td>
</tr>
</table>

## -remarks

This method must be implemented to allow cut, copy, paste, drag, and drop operations of Component Object Model (COM) objects.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditolecallback">IRichEditOleCallback</a>



<b>Reference</b>