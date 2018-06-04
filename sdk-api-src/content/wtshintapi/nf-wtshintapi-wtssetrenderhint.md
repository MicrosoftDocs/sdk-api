---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

<i>pHintData</i> contains a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure 
          which specifies the coordinates and size of the rendering area. These per-monitor DPI-aware coordinates are 
          relative to the client coordinates of the window represented by the <i>hwndOwner</i> 
          parameter.

<b>Windows 8 and Windows Server 2012:  </b>The coordinates are not DPI-aware before Windows 8.1 and 
          Windows Server 2012 R2.



#### RENDER_HINT_MAPPEDWINDOW (2)

Indicates the presence of a window mapping.

<i>pHintData</i> contains a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure 
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



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



