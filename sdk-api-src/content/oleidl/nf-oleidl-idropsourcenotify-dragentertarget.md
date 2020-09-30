---
UID: NF:oleidl.IDropSourceNotify.DragEnterTarget
title: IDropSourceNotify::DragEnterTarget (oleidl.h)
description: OLE calls this method when the user drags the mouse cursor into a potential drop target window.
helpviewer_keywords: ["DragEnterTarget","DragEnterTarget method [COM]","DragEnterTarget method [COM]","IDropSourceNotify interface","IDropSourceNotify interface [COM]","DragEnterTarget method","IDropSourceNotify.DragEnterTarget","IDropSourceNotify::DragEnterTarget","_ole_idropsourcenotify_dragentertarget","com.idropsourcenotify_dragentertarget","oleidl/IDropSourceNotify::DragEnterTarget"]
old-location: com\idropsourcenotify_dragentertarget.htm
tech.root: com
ms.assetid: 2f2ca860-1f63-4cc1-9a9e-4efb6fceb867
ms.date: 12/05/2018
ms.keywords: DragEnterTarget, DragEnterTarget method [COM], DragEnterTarget method [COM],IDropSourceNotify interface, IDropSourceNotify interface [COM],DragEnterTarget method, IDropSourceNotify.DragEnterTarget, IDropSourceNotify::DragEnterTarget, _ole_idropsourcenotify_dragentertarget, com.idropsourcenotify_dragentertarget, oleidl/IDropSourceNotify::DragEnterTarget
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IDropSourceNotify::DragEnterTarget
 - oleidl/IDropSourceNotify::DragEnterTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IDropSourceNotify.DragEnterTarget
---

# IDropSourceNotify::DragEnterTarget


## -description

OLE calls this method when the user drags the mouse cursor into a potential drop target window.

## -parameters

### -param hwndTarget [in]

The window handle of the potential drop target window.

## -returns

This method returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsourcenotify">IDropSourceNotify</a>