---
UID: NE:strmif._AM_OVERLAY_NOTIFY_FLAGS
title: "_AM_OVERLAY_NOTIFY_FLAGS (strmif.h)"
description: The AM_OVERLAY_NOTIFY_FLAGS enumeration indicates what the overlay has changed, or is about to change.
helpviewer_keywords: ["AM_OVERLAY_NOTIFY_DEST_CHANGE","AM_OVERLAY_NOTIFY_FLAGS","AM_OVERLAY_NOTIFY_FLAGSEnumeration","AM_OVERLAY_NOTIFY_SOURCE_CHANGE","AM_OVERLAY_NOTIFY_VISIBLE_CHANGE","_AM_OVERLAY_NOTIFY_FLAGS","_AM_OVERLAY_NOTIFY_FLAGS enumeration [DirectShow]","dshow.am_overlay_notify_flags","strmif/AM_OVERLAY_NOTIFY_DEST_CHANGE","strmif/AM_OVERLAY_NOTIFY_SOURCE_CHANGE","strmif/AM_OVERLAY_NOTIFY_VISIBLE_CHANGE","strmif/_AM_OVERLAY_NOTIFY_FLAGS"]
old-location: dshow\am_overlay_notify_flags.htm
tech.root: dshow
ms.assetid: bc16714b-acee-4b5d-aa1d-6b53965183dc
ms.date: 12/05/2018
ms.keywords: AM_OVERLAY_NOTIFY_DEST_CHANGE, AM_OVERLAY_NOTIFY_FLAGS, AM_OVERLAY_NOTIFY_FLAGSEnumeration, AM_OVERLAY_NOTIFY_SOURCE_CHANGE, AM_OVERLAY_NOTIFY_VISIBLE_CHANGE, _AM_OVERLAY_NOTIFY_FLAGS, _AM_OVERLAY_NOTIFY_FLAGS enumeration [DirectShow], dshow.am_overlay_notify_flags, strmif/AM_OVERLAY_NOTIFY_DEST_CHANGE, strmif/AM_OVERLAY_NOTIFY_SOURCE_CHANGE, strmif/AM_OVERLAY_NOTIFY_VISIBLE_CHANGE, strmif/_AM_OVERLAY_NOTIFY_FLAGS
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_OVERLAY_NOTIFY_FLAGS
 - strmif/_AM_OVERLAY_NOTIFY_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strmif.h
api_name:
 - _AM_OVERLAY_NOTIFY_FLAGS
---

# _AM_OVERLAY_NOTIFY_FLAGS enumeration


## -description

The AM_OVERLAY_NOTIFY_FLAGS enumeration indicates what the overlay has changed, or is about to change.

## -enum-fields

### -field AM_OVERLAY_NOTIFY_VISIBLE_CHANGE:0x1

The rectangle will be changed from visible to invisible, or vice-versa.

### -field AM_OVERLAY_NOTIFY_SOURCE_CHANGE:0x2

Source rectangle changed or changing.

### -field AM_OVERLAY_NOTIFY_DEST_CHANGE:0x4

Destination rectangle changed or changing.

## -remarks

The <a href="/windows/win32/api/strmif/nf-strmif-iddrawexclmodevideocallback-onupdateoverlay">IDDrawExclModeVideoCallback::OnUpdateOverlay</a> method uses these flags to indicate how the overlay has changed, so that applications can take the necessary steps.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/win32/api/strmif/nf-strmif-iddrawexclmodevideocallback-onupdateoverlay">IDDrawExclModeVideoCallback::OnUpdateOverlay</a>
