---
UID: NF:ddrawgdi.DdQueryDisplaySettingsUniqueness
title: DdQueryDisplaySettingsUniqueness function
author: windows-sdk-content
description: Returns the current value of an integer that is incremented whenever a mode switch occurs, such as when there is a desktop switch, a Fast User Switch, or a full-screen Microsoft MS-DOS box.
old-location: winprog\_dxgkernel_ddquerydisplaysettingsuniqueness.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddquerydisplaysettingsuniqueness.htm
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: DdQueryDisplaySettingsUniqueness, DdQueryDisplaySettingsUniqueness function [Windows API], GdiEntry13, _dxgkernel_ddquerydisplaysettingsuniqueness, ddrawgdi/DdQueryDisplaySettingsUniqueness, ddrawgdi/GdiEntry13, winprog._dxgkernel_ddquerydisplaysettingsuniqueness, winui._dxgkernel_ddquerydisplaysettingsuniqueness
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


## -parameters






## -returns



The current value of the mode switch integer is returned.




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

