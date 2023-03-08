---
UID: NF:ddraw.IDirectDraw7.EnumDisplayModes
title: IDirectDraw7::EnumDisplayModes (ddraw.h)
description: Enumerates all the display modes that the hardware exposes through the DirectDraw object and that are compatible with a provided surface description.
helpviewer_keywords: ["DDEDM_REFRESHRATES","DDEDM_STANDARDVGAMODES","EnumDisplayModes","EnumDisplayModes method [DirectDraw]","EnumDisplayModes method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","EnumDisplayModes method","IDirectDraw7.EnumDisplayModes","IDirectDraw7::EnumDisplayModes","ddraw/IDirectDraw7::EnumDisplayModes","directdraw.idirectdraw7_enumdisplaymodes"]
old-location: directdraw\idirectdraw7_enumdisplaymodes.htm
tech.root: directdraw
ms.assetid: 04ed2545-c611-435d-95ef-a0d854380a69
ms.date: 12/05/2018
ms.keywords: DDEDM_REFRESHRATES, DDEDM_STANDARDVGAMODES, EnumDisplayModes, EnumDisplayModes method [DirectDraw], EnumDisplayModes method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],EnumDisplayModes method, IDirectDraw7.EnumDisplayModes, IDirectDraw7::EnumDisplayModes, ddraw/IDirectDraw7::EnumDisplayModes, directdraw.idirectdraw7_enumdisplaymodes
req.header: ddraw.h
req.include-header: 
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDraw7::EnumDisplayModes
 - ddraw/IDirectDraw7::EnumDisplayModes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.EnumDisplayModes
---

# IDirectDraw7::EnumDisplayModes


## -description

Enumerates all the display modes that the hardware exposes through the DirectDraw object and that are compatible with a provided surface description.

## -parameters

### -param unnamedParam1 [in]

This value consists of one or more of the following flags:



#### DDEDM_REFRESHRATES

Enumerates modes with different refresh rates. <b>IDirectDraw7::EnumDisplayModes</b> guarantees that a particular mode is enumerated only once. This flag specifies whether the refresh rate is taken into account when determining whether a mode is unique.



#### DDEDM_STANDARDVGAMODES

Enumerates Mode 13 in addition to the 320x200x8 Mode X mode.

### -param unnamedParam2 [in]

Address of a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure to be checked against available modes. If the value of this parameter is NULL, all modes are enumerated.

### -param unnamedParam3 [in]

Address of an application-defined structure to be passed to each enumeration member.

### -param unnamedParam4 [in]

Address of the <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenummodescallback2">EnumModesCallback2</a> function that the enumeration procedure calls every time a match is found.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks

<b>IDirectDraw7::EnumDisplayModes</b> enumerates the <b>dwRefreshRate</b> member of the <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure; the IDirectDraw::EnumDisplayModes method does not have this ability. If you use the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-setdisplaymode">IDirectDraw7::SetDisplayMode</a> method to set the refresh rate of a new mode, use <b>IDirectDraw7::EnumDisplayModes</b> to enumerate the <b>dwRefreshRate</b> member.



<b>IDirectDraw7::EnumDisplayModes</b> differs from its counterparts in former interfaces in that it accepts the address of an <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenummodescallback2">EnumModesCallback2</a> function as a parameter, rather than an <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenummodescallback">EnumModesCallback</a> function.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>