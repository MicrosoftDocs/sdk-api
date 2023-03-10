---
UID: NE:dxgidebug.DXGI_DEBUG_RLO_FLAGS
title: DXGI_DEBUG_RLO_FLAGS (dxgidebug.h)
description: Flags used with ReportLiveObjects to specify the amount of info to report about an object's lifetime.
helpviewer_keywords: ["DXGI_DEBUG_RLO_ALL","DXGI_DEBUG_RLO_DETAIL","DXGI_DEBUG_RLO_FLAGS","DXGI_DEBUG_RLO_FLAGS enumeration [DXGI]","DXGI_DEBUG_RLO_IGNORE_INTERNAL","DXGI_DEBUG_RLO_SUMMARY","direct3ddxgi.dxgi_debug_rlo_flags","dxgidebug/DXGI_DEBUG_RLO_ALL","dxgidebug/DXGI_DEBUG_RLO_DETAIL","dxgidebug/DXGI_DEBUG_RLO_FLAGS","dxgidebug/DXGI_DEBUG_RLO_IGNORE_INTERNAL","dxgidebug/DXGI_DEBUG_RLO_SUMMARY"]
old-location: direct3ddxgi\dxgi_debug_rlo_flags.htm
tech.root: direct3ddxgi
ms.assetid: 8A4B4139-42FC-4983-9699-ABCDBF5783E7
ms.date: 12/05/2018
ms.keywords: DXGI_DEBUG_RLO_ALL, DXGI_DEBUG_RLO_DETAIL, DXGI_DEBUG_RLO_FLAGS, DXGI_DEBUG_RLO_FLAGS enumeration [DXGI], DXGI_DEBUG_RLO_IGNORE_INTERNAL, DXGI_DEBUG_RLO_SUMMARY, direct3ddxgi.dxgi_debug_rlo_flags, dxgidebug/DXGI_DEBUG_RLO_ALL, dxgidebug/DXGI_DEBUG_RLO_DETAIL, dxgidebug/DXGI_DEBUG_RLO_FLAGS, dxgidebug/DXGI_DEBUG_RLO_IGNORE_INTERNAL, dxgidebug/DXGI_DEBUG_RLO_SUMMARY
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: DXGI_DEBUG_RLO_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_DEBUG_RLO_FLAGS
 - dxgidebug/DXGI_DEBUG_RLO_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGIDebug.h
api_name:
 - DXGI_DEBUG_RLO_FLAGS
---

# DXGI_DEBUG_RLO_FLAGS enumeration


## -description

Flags used with <a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgidebug-reportliveobjects">ReportLiveObjects</a> to specify the amount of info to report about an object's lifetime.

## -enum-fields

### -field DXGI_DEBUG_RLO_SUMMARY:0x1

A flag that specifies to obtain a summary about an object's lifetime.

### -field DXGI_DEBUG_RLO_DETAIL:0x2

A flag that specifies to obtain detailed info about an object's lifetime.

### -field DXGI_DEBUG_RLO_IGNORE_INTERNAL:0x4

This flag indicates to ignore objects which have no external refcounts keeping them alive.
            D3D objects are printed using an external refcount and an internal refcount. 
            Typically, all objects are printed. 
            This flag means ignore the objects whose external refcount is 0, because the application is not responsible for keeping them alive.

### -field DXGI_DEBUG_RLO_ALL:0x7

A flag that specifies to obtain both a summary and detailed info about an object's lifetime.

## -remarks

Use this enumeration with <a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgidebug-reportliveobjects">IDXGIDebug::ReportLiveObjects</a>.
        

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>
