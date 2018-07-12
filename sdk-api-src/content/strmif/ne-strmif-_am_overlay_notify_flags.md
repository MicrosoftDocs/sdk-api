---
UID: NE:strmif._AM_OVERLAY_NOTIFY_FLAGS
title: "_AM_OVERLAY_NOTIFY_FLAGS"
author: windows-sdk-content
description: The AM_OVERLAY_NOTIFY_FLAGS enumeration indicates what the overlay has changed, or is about to change.
old-location: dshow\am_overlay_notify_flags.htm
old-project: DirectShow
ms.assetid: bc16714b-acee-4b5d-aa1d-6b53965183dc
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: AM_OVERLAY_NOTIFY_DEST_CHANGE, AM_OVERLAY_NOTIFY_FLAGS, AM_OVERLAY_NOTIFY_FLAGSEnumeration, AM_OVERLAY_NOTIFY_SOURCE_CHANGE, AM_OVERLAY_NOTIFY_VISIBLE_CHANGE, _AM_OVERLAY_NOTIFY_FLAGS, _AM_OVERLAY_NOTIFY_FLAGS enumeration [DirectShow], dshow.am_overlay_notify_flags, strmif/AM_OVERLAY_NOTIFY_DEST_CHANGE, strmif/AM_OVERLAY_NOTIFY_SOURCE_CHANGE, strmif/AM_OVERLAY_NOTIFY_VISIBLE_CHANGE, strmif/_AM_OVERLAY_NOTIFY_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strmif.h
api_name:
 - _AM_OVERLAY_NOTIFY_FLAGS
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1
---

# _AM_OVERLAY_NOTIFY_FLAGS enumeration


## -description



The AM_OVERLAY_NOTIFY_FLAGS enumeration indicates what the overlay has changed, or is about to change.




## -enum-fields




### -field AM_OVERLAY_NOTIFY_VISIBLE_CHANGE

The rectangle will be changed from visible to invisible, or vice-versa.


### -field AM_OVERLAY_NOTIFY_SOURCE_CHANGE

Source rectangle changed or changing.


### -field AM_OVERLAY_NOTIFY_DEST_CHANGE

Destination rectangle changed or changing.


## -remarks



The <a href="https://msdn.microsoft.com/ede823ba-8340-4339-8e8a-e1d4f9ad1273">IDDrawExclModeVideoCallback::OnUpdateOverlay</a> method uses these flags to indicate how the overlay has changed, so that applications can take the necessary steps.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/ede823ba-8340-4339-8e8a-e1d4f9ad1273">IDDrawExclModeVideoCallback::OnUpdateOverlay</a>
 

 

