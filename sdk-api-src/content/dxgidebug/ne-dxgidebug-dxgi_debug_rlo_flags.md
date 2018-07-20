---
UID: NE:dxgidebug.DXGI_DEBUG_RLO_FLAGS
title: DXGI_DEBUG_RLO_FLAGS
author: windows-sdk-content
description: Flags used with ReportLiveObjects to specify the amount of info to report about an object's lifetime.
old-location: direct3ddxgi\dxgi_debug_rlo_flags.htm
old-project: direct3ddxgi
ms.assetid: 8A4B4139-42FC-4983-9699-ABCDBF5783E7
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DXGI_DEBUG_RLO_ALL, DXGI_DEBUG_RLO_DETAIL, DXGI_DEBUG_RLO_FLAGS, DXGI_DEBUG_RLO_FLAGS enumeration [DXGI], DXGI_DEBUG_RLO_IGNORE_INTERNAL, DXGI_DEBUG_RLO_SUMMARY, direct3ddxgi.dxgi_debug_rlo_flags, dxgidebug/DXGI_DEBUG_RLO_ALL, dxgidebug/DXGI_DEBUG_RLO_DETAIL, dxgidebug/DXGI_DEBUG_RLO_FLAGS, dxgidebug/DXGI_DEBUG_RLO_IGNORE_INTERNAL, dxgidebug/DXGI_DEBUG_RLO_SUMMARY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: DXGI_DEBUG_RLO_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGIDebug.h
api_name:
 - DXGI_DEBUG_RLO_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_DEBUG_RLO_FLAGS enumeration


## -description


Flags used with <a href="https://msdn.microsoft.com/6CA5C335-08E3-4CC6-A9C9-D7BC6B11C0EA">ReportLiveObjects</a> to specify the amount of info to report about an object's lifetime.
        


## -enum-fields




### -field DXGI_DEBUG_RLO_SUMMARY

A flag that specifies to obtain a summary about an object's lifetime.
          


### -field DXGI_DEBUG_RLO_DETAIL

A flag that specifies to obtain detailed info about an object's lifetime.
          


### -field DXGI_DEBUG_RLO_IGNORE_INTERNAL

This flag indicates to ignore objects which have no external refcounts keeping them alive.
            D3D objects are printed using an external refcount and an internal refcount. 
            Typically, all objects are printed. 
            This flag means ignore the objects whose external refcount is 0, because the application is not responsible for keeping them alive.
          


### -field DXGI_DEBUG_RLO_ALL

A flag that specifies to obtain both a summary and detailed info about an object's lifetime.
          


## -remarks



Use this enumeration with <a href="https://msdn.microsoft.com/6CA5C335-08E3-4CC6-A9C9-D7BC6B11C0EA">IDXGIDebug::ReportLiveObjects</a>.
        

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

