---
UID: NF:ddrawgdi.DdQueryDisplaySettingsUniqueness
title: DdQueryDisplaySettingsUniqueness function (ddrawgdi.h)
description: Returns the current value of an integer that is incremented whenever a mode switch occurs, such as when there is a desktop switch, a Fast User Switch, or a full-screen Microsoft MS-DOS box.
helpviewer_keywords: ["DdQueryDisplaySettingsUniqueness","DdQueryDisplaySettingsUniqueness function [Windows API]","GdiEntry13","_dxgkernel_ddquerydisplaysettingsuniqueness","ddrawgdi/DdQueryDisplaySettingsUniqueness","ddrawgdi/GdiEntry13","winprog._dxgkernel_ddquerydisplaysettingsuniqueness","winui._dxgkernel_ddquerydisplaysettingsuniqueness"]
old-location: winprog\_dxgkernel_ddquerydisplaysettingsuniqueness.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddquerydisplaysettingsuniqueness.htm
ms.date: 12/05/2018
ms.keywords: DdQueryDisplaySettingsUniqueness, DdQueryDisplaySettingsUniqueness function [Windows API], GdiEntry13, _dxgkernel_ddquerydisplaysettingsuniqueness, ddrawgdi/DdQueryDisplaySettingsUniqueness, ddrawgdi/GdiEntry13, winprog._dxgkernel_ddquerydisplaysettingsuniqueness, winui._dxgkernel_ddquerydisplaysettingsuniqueness
req.header: ddrawgdi.h
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
req.dll: GDI32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdQueryDisplaySettingsUniqueness
 - ddrawgdi/DdQueryDisplaySettingsUniqueness
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - GDI32.dll
 - API-MS-Win-DX-D3DKMT-L1-1-0.dll
 - API-MS-Win-DX-D3DKMT-L1-1-1.dll
 - API-MS-Win-DX-D3DKMT-L1-1-2.dll
api_name:
 - DdQueryDisplaySettingsUniqueness
 - GdiEntry13
---

# DdQueryDisplaySettingsUniqueness function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use 
    the Microsoft DirectDraw and Microsoft Direct3DAPIs; these 
    APIs insulate applications from such operating system changes, and hide many other 
    difficulties involved in interacting directly with display drivers.]

Returns the current value of an integer that is incremented whenever a mode switch occurs, such as when there 
    is a desktop switch, a Fast User Switch, or a full-screen Microsoft MS-DOS box. The application can call 
    this function repeatedly and compare the old and new values of the return value to determine whether display 
    settings have changed.

<b>GdiEntry13</b> is defined as an alias for this function.



## -returns

The current value of the mode switch integer is returned.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>
