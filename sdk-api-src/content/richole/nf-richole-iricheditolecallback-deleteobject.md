---
UID: NF:richole.IRichEditOleCallback.DeleteObject
title: IRichEditOleCallback::DeleteObject (richole.h)
description: Sends notification that an object is about to be deleted from a rich edit control. The object is not necessarily being released when this member is called.
helpviewer_keywords: ["DeleteObject","DeleteObject method [Windows Controls]","DeleteObject method [Windows Controls]","IRichEditOleCallback interface","IRichEditOleCallback interface [Windows Controls]","DeleteObject method","IRichEditOleCallback.DeleteObject","IRichEditOleCallback::DeleteObject","_win32_IRichEditOleCallback_DeleteObject","_win32_IRichEditOleCallback_DeleteObject_cpp","controls.IRichEditOleCallback_DeleteObject","controls._win32_IRichEditOleCallback_DeleteObject","richole/IRichEditOleCallback::DeleteObject"]
old-location: controls\IRichEditOleCallback_DeleteObject.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackdeleteobject.htm
ms.date: 12/05/2018
ms.keywords: DeleteObject, DeleteObject method [Windows Controls], DeleteObject method [Windows Controls],IRichEditOleCallback interface, IRichEditOleCallback interface [Windows Controls],DeleteObject method, IRichEditOleCallback.DeleteObject, IRichEditOleCallback::DeleteObject, _win32_IRichEditOleCallback_DeleteObject, _win32_IRichEditOleCallback_DeleteObject_cpp, controls.IRichEditOleCallback_DeleteObject, controls._win32_IRichEditOleCallback_DeleteObject, richole/IRichEditOleCallback::DeleteObject
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
 - IRichEditOleCallback::DeleteObject
 - richole/IRichEditOleCallback::DeleteObject
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
 - IRichEditOleCallback.DeleteObject
---

# IRichEditOleCallback::DeleteObject


## -description

Sends notification that an object is about to be deleted from a rich edit control. The object is not necessarily being released when this member is called.

## -parameters

### -param lpoleobj

Type: <b>LPOLEOBJECT</b>

The object that is being deleted.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditolecallback">IRichEditOleCallback</a>