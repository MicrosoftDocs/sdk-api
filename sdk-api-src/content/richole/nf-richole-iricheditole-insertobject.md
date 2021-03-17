---
UID: NF:richole.IRichEditOle.InsertObject
title: IRichEditOle::InsertObject (richole.h)
description: Inserts an object into a rich edit control.
helpviewer_keywords: ["IRichEditOle interface [Windows Controls]","InsertObject method","IRichEditOle.InsertObject","IRichEditOle::InsertObject","InsertObject","InsertObject method [Windows Controls]","InsertObject method [Windows Controls]","IRichEditOle interface","_win32_IRichEditOle_InsertObject","_win32_IRichEditOle_InsertObject_cpp","controls.IRichEditOle_InsertObject","controls._win32_IRichEditOle_InsertObject","richole/IRichEditOle::InsertObject"]
old-location: controls\IRichEditOle_InsertObject.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditoleinsertobject.htm
ms.date: 12/05/2018
ms.keywords: IRichEditOle interface [Windows Controls],InsertObject method, IRichEditOle.InsertObject, IRichEditOle::InsertObject, InsertObject, InsertObject method [Windows Controls], InsertObject method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_InsertObject, _win32_IRichEditOle_InsertObject_cpp, controls.IRichEditOle_InsertObject, controls._win32_IRichEditOle_InsertObject, richole/IRichEditOle::InsertObject
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
 - IRichEditOle::InsertObject
 - richole/IRichEditOle::InsertObject
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
 - IRichEditOle.InsertObject
---

# IRichEditOle::InsertObject


## -description

Inserts an object into a rich edit control.

## -parameters

### -param lpreobject

Type: <b><a href="/windows/desktop/api/richole/ns-richole-reobject">REOBJECT</a>*</b>

The object information and interfaces. The rich edit control automatically increments the reference count for the interfaces if it holds onto them, so the caller can safely release the interfaces if they are not needed.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_OUTOFMEMORY is returned if memory could not be allocated to insert the object.

## -remarks

If the <b>cp</b> member of the <a href="/windows/desktop/api/richole/ns-richole-reobject">REOBJECT</a> structure is REO_CP_SELECTION, the selection is replaced with the specified object.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>



<a href="/windows/desktop/api/richole/ns-richole-reobject">REOBJECT</a>



<b>Reference</b>