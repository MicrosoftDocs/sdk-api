---
UID: NF:wtshintapi.WTSSetRenderHint
title: WTSSetRenderHint function (wtshintapi.h)
description: Used by an application that is displaying content that can be optimized for displaying in a remote session to identify the region of a window that is the actual content.
helpviewer_keywords: ["RENDER_HINT_CLEAR","RENDER_HINT_MAPPEDWINDOW","RENDER_HINT_VIDEO","WTSSetRenderHint","WTSSetRenderHint function [Remote Desktop Services]","termserv.wtssetrenderhint","wtshintapi/WTSSetRenderHint"]
old-location: termserv\wtssetrenderhint.htm
tech.root: TermServ
ms.assetid: CF8AE408-AE3A-44AC-91F9-6F6D9858893F
ms.date: 12/05/2018
ms.keywords: RENDER_HINT_CLEAR, RENDER_HINT_MAPPEDWINDOW, RENDER_HINT_VIDEO, WTSSetRenderHint, WTSSetRenderHint function [Remote Desktop Services], termserv.wtssetrenderhint, wtshintapi/WTSSetRenderHint
req.header: wtshintapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WtsApi32.lib
req.dll: WtsApi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSSetRenderHint
 - wtshintapi/WTSSetRenderHint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WtsApi32.dll
api_name:
 - WTSSetRenderHint
---

# WTSSetRenderHint function


## -description

Used by an application that is displaying content that can be optimized for displaying in a remote 
    session to identify the region of a window that is the actual content.

In the remote session, this content will be encoded, sent to the client, then decoded and displayed.

## -parameters

### -param pRenderHintID [in, out]

The address of a value that identifies the rendering hint affected by this call. If a new hint is being 
      created, this value must contain zero. This function will return a unique rendering hint identifier which is 
      used for subsequent calls, such as clearing the hint.

### -param hwndOwner [in]

The handle of window linked to lifetime of the rendering hint. This window is used in situations where a 
      hint target is removed without the hint being explicitly cleared.

### -param renderHintType [in]

Specifies the type of hint represented by this call.



#### RENDER_HINT_CLEAR (0)

The previous hint is cleared.

<i>pHintData</i> must be <b>NULL</b>.



#### RENDER_HINT_VIDEO (1)

Indicates the presence of moving video.

<i>pHintData</i> contains a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure 
          which specifies the coordinates and size of the rendering area. These per-monitor DPI-aware coordinates are 
          relative to the client coordinates of the window represented by the <i>hwndOwner</i> 
          parameter.

<b>Windows 8 and Windows Server 2012:  </b>The coordinates are not DPI-aware before Windows 8.1 and 
          Windows Server 2012 R2.



#### RENDER_HINT_MAPPEDWINDOW (2)

Indicates the presence of a window mapping.

<i>pHintData</i> contains a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure 
         which specifies the coordinates and size of the rendering area. These per-monitor DPI-aware coordinates are 
         relative to the client coordinates of the window represented by the <i>hwndOwner</i> 
         parameter.

<b>Windows 8 and Windows Server 2012:  </b>The coordinates are not DPI-aware before Windows 8.1 and 
          Windows Server 2012 R2.

### -param cbHintDataLength [in]

The size, in <b>BYTE</b>s, of the <i>pHintData</i> buffer.

### -param pHintData [in]

Additional data for the hint.

The format of this data is dependent upon the value passed in the <i>renderHintType</i> 
       parameter.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

