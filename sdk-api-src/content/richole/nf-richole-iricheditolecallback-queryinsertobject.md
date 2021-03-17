---
UID: NF:richole.IRichEditOleCallback.QueryInsertObject
title: IRichEditOleCallback::QueryInsertObject (richole.h)
description: Queries the application as to whether an object should be inserted. The member is called when pasting and when reading Rich Text Format (RTF).
helpviewer_keywords: ["IRichEditOleCallback interface [Windows Controls]","QueryInsertObject method","IRichEditOleCallback.QueryInsertObject","IRichEditOleCallback::QueryInsertObject","QueryInsertObject","QueryInsertObject method [Windows Controls]","QueryInsertObject method [Windows Controls]","IRichEditOleCallback interface","_win32_IRichEditOleCallback_QueryInsertObject","_win32_IRichEditOleCallback_QueryInsertObject_cpp","controls.IRichEditOleCallback_QueryInsertObject","controls._win32_IRichEditOleCallback_QueryInsertObject","richole/IRichEditOleCallback::QueryInsertObject"]
old-location: controls\IRichEditOleCallback_QueryInsertObject.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackqueryinsertobject.htm
ms.date: 12/05/2018
ms.keywords: IRichEditOleCallback interface [Windows Controls],QueryInsertObject method, IRichEditOleCallback.QueryInsertObject, IRichEditOleCallback::QueryInsertObject, QueryInsertObject, QueryInsertObject method [Windows Controls], QueryInsertObject method [Windows Controls],IRichEditOleCallback interface, _win32_IRichEditOleCallback_QueryInsertObject, _win32_IRichEditOleCallback_QueryInsertObject_cpp, controls.IRichEditOleCallback_QueryInsertObject, controls._win32_IRichEditOleCallback_QueryInsertObject, richole/IRichEditOleCallback::QueryInsertObject
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
 - IRichEditOleCallback::QueryInsertObject
 - richole/IRichEditOleCallback::QueryInsertObject
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
 - IRichEditOleCallback.QueryInsertObject
---

# IRichEditOleCallback::QueryInsertObject


## -description

Queries the application as to whether an object should be inserted. The member is called when pasting and when reading Rich Text Format (RTF).

## -parameters

### -param lpclsid

Type: <b>LPCLSID</b>

Class identifier of the object to be inserted.

### -param lpstg

Type: <b>LPSTORAGE</b>

Storage containing the object.

### -param cp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Character position, at which the object will be inserted.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success. If the return value is not S_OK, the object was not inserted. If the method fails, it can return the following value.

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
</table>

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditolecallback">IRichEditOleCallback</a>