---
UID: NS:oleidl.tagOIFI
title: OLEINPLACEFRAMEINFO (oleidl.h)
description: Contains information about the accelerators supported by a container during an in-place session. The structure is used in the IOleInPlaceSite::GetWindowContext method and the OleTranslateAccelerator function.
helpviewer_keywords: ["*LPOLEINPLACEFRAMEINFO","LPOLEINPLACEFRAMEINFO","LPOLEINPLACEFRAMEINFO structure pointer [COM]","OLEINPLACEFRAMEINFO","OLEINPLACEFRAMEINFO structure [COM]","_ole_OLEINPLACEFRAMEINFO","com.oleinplaceframeinfo","oleidl/LPOLEINPLACEFRAMEINFO","oleidl/OLEINPLACEFRAMEINFO"]
old-location: com\oleinplaceframeinfo.htm
tech.root: com
ms.assetid: e09445d2-61e5-4691-b51e-746e0cc91c00
ms.date: 12/05/2018
ms.keywords: '*LPOLEINPLACEFRAMEINFO, LPOLEINPLACEFRAMEINFO, LPOLEINPLACEFRAMEINFO structure pointer [COM], OLEINPLACEFRAMEINFO, OLEINPLACEFRAMEINFO structure [COM], _ole_OLEINPLACEFRAMEINFO, com.oleinplaceframeinfo, oleidl/LPOLEINPLACEFRAMEINFO, oleidl/OLEINPLACEFRAMEINFO'
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEINPLACEFRAMEINFO, *LPOLEINPLACEFRAMEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOIFI
 - oleidl/tagOIFI
 - LPOLEINPLACEFRAMEINFO
 - oleidl/LPOLEINPLACEFRAMEINFO
 - OLEINPLACEFRAMEINFO
 - oleidl/OLEINPLACEFRAMEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLEINPLACEFRAMEINFO
---

# OLEINPLACEFRAMEINFO structure


## -description

Contains information about the accelerators supported by a container during an in-place session. The structure is used in the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-getwindowcontext">IOleInPlaceSite::GetWindowContext</a> method and the <a href="/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a> function.

## -struct-fields

### -field cb

The size of this structure, in bytes. The object server must specify sizeof(<b>OLEINPLACEFRAMEINFO</b>) in the structure it passes to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-getwindowcontext">IOleInPlaceSite::GetWindowContext</a>. The container can then use this size to determine the structure's version.

### -field fMDIApp

Indicates whether the container is an MDI application.

### -field hwndFrame

A handle to the container's top-level frame window.

### -field haccel

A handle to the accelerator table that the container wants to use during an in-place editing session.

### -field cAccelEntries

The number of accelerators in <b>haccel</b>.

## -remarks

When an object is being in-place activated, its server calls the container's <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-getwindowcontext">IOleInPlaceSite::GetWindowContext</a> method, which fills in an <b>OLEINPLACEFRAMEINFO</b> structure. During an in-place session, the message loop of an EXE server passes a pointer to the <b>OLEINPLACEFRAMEINFO</b> structure to <a href="/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a>. OLE uses the information in this structure to determine whether a message maps to one of the container's accelerators.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-getwindowcontext">IOleInPlaceSite::GetWindowContext</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a>