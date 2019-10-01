---
UID: NF:wingdi.DeleteDC
title: DeleteDC function (wingdi.h)
author: windows-sdk-content
description: The DeleteDC function deletes the specified device context (DC).
old-location: gdi\deletedc.htm
tech.root: gdi
ms.assetid: 1aa549a0-c95f-4385-a30e-8906f67e39cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteDC, DeleteDC function [Windows GDI], _win32_DeleteDC, gdi.deletedc, wingdi/DeleteDC
ms.topic: function
f1_keywords: 
 - "wingdi/DeleteDC"
req.header: wingdi.h
req.include-header: Windows.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-Create-l1-1-0.dll
 - Ext-MS-Win-GDI-DC-Create-l1-1-1.dll
 - ext-ms-win-gdi-dc-create-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - DeleteDC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteDC function


## -description


The <b>DeleteDC</b> function deletes the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



An application must not delete a DC whose handle was obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a> function. Instead, it must call the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-releasedc">ReleaseDC</a> function to free the DC.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/gdi/retrieving-the-capabilities-of-a-printer">Retrieving the Capabilities of a Printer</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-releasedc">ReleaseDC</a>
 

 

