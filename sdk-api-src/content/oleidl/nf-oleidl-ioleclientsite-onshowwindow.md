---
UID: NF:oleidl.IOleClientSite.OnShowWindow
title: IOleClientSite::OnShowWindow (oleidl.h)
description: Notifies a container when an embedded object's window is about to become visible or invisible. This method does not apply to an object that is activated in place and therefore has no window separate from that of its container.
helpviewer_keywords: ["IOleClientSite interface [COM]","OnShowWindow method","IOleClientSite.OnShowWindow","IOleClientSite::OnShowWindow","OnShowWindow","OnShowWindow method [COM]","OnShowWindow method [COM]","IOleClientSite interface","_ole_ioleclientsite_onshowwindow","com.ioleclientsite_onshowwindow","oleidl/IOleClientSite::OnShowWindow"]
old-location: com\ioleclientsite_onshowwindow.htm
tech.root: com
ms.assetid: 9185add8-02d1-4bf3-99ff-82f64ba12ef4
ms.date: 12/05/2018
ms.keywords: IOleClientSite interface [COM],OnShowWindow method, IOleClientSite.OnShowWindow, IOleClientSite::OnShowWindow, OnShowWindow, OnShowWindow method [COM], OnShowWindow method [COM],IOleClientSite interface, _ole_ioleclientsite_onshowwindow, com.ioleclientsite_onshowwindow, oleidl/IOleClientSite::OnShowWindow
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IOleClientSite::OnShowWindow
 - oleidl/IOleClientSite::OnShowWindow
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
 - IOleClientSite.OnShowWindow
---

# IOleClientSite::OnShowWindow


## -description

Notifies a container when an embedded object's window is about to become visible or invisible. This method does not apply to an object that is activated in place and therefore has no window separate from that of its container.

## -parameters

### -param fShow [in]

Indicates whether an object's window is open (TRUE) or closed (FALSE).

## -returns

This method returns S_OK on success.

## -remarks

An embedded object calls <b>OnShowWindow</b> to keep its container informed when the object is open in a window. This window may or may not be currently visible to the end user. The container uses this information to shade the object's client site when the object is displayed in a window, and to remove the shading when the object is not. A shaded object, having received this notification, knows that it already has an open window and therefore can respond to being double-clicked by bringing this window quickly to the top, instead of launching its application in order to obtain a new one.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>