---
UID: NS:shellapi._AppBarData
title: APPBARDATA (shellapi.h)
description: Contains information about a system appbar message.
helpviewer_keywords: ["*PAPPBARDATA","ABE_BOTTOM","ABE_LEFT","ABE_RIGHT","ABE_TOP","APPBARDATA","APPBARDATA structure [Windows Shell]","PAPPBARDATA","PAPPBARDATA structure pointer [Windows Shell]","_win32_APPBARDATA","shell.APPBARDATA","shellapi/APPBARDATA","shellapi/PAPPBARDATA"]
old-location: shell\APPBARDATA.htm
tech.root: shell
ms.assetid: cf86fe15-4beb-49b7-b73e-2ad61cedc3f8
ms.date: 12/05/2018
ms.keywords: '*PAPPBARDATA, ABE_BOTTOM, ABE_LEFT, ABE_RIGHT, ABE_TOP, APPBARDATA, APPBARDATA structure [Windows Shell], PAPPBARDATA, PAPPBARDATA structure pointer [Windows Shell], _win32_APPBARDATA, shell.APPBARDATA, shellapi/APPBARDATA, shellapi/PAPPBARDATA'
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: APPBARDATA, *PAPPBARDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AppBarData
 - shellapi/_AppBarData
 - PAPPBARDATA
 - shellapi/PAPPBARDATA
 - APPBARDATA
 - shellapi/APPBARDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - APPBARDATA
---

# APPBARDATA structure


## -description

Contains information about a system appbar message.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes.

### -field hWnd

Type: <b>HWND</b>

The handle to the appbar window. Not all messages use this member. See the individual message page to see if you need to provide an <b>hWind</b> value.

### -field uCallbackMessage

Type: <b>UINT</b>

An application-defined message identifier. The application uses the specified identifier for notification messages that it sends to the appbar identified by the <b>hWnd</b> member. This member is used when sending the <a href="/windows/desktop/shell/abm-new">ABM_NEW</a> message.

### -field uEdge

Type: <b>UINT</b>

A value that specifies an edge of the screen. This member is used when sending one of these messages:
                        
<ul>
<li>
<a href="/windows/desktop/shell/abm-getautohidebar">ABM_GETAUTOHIDEBAR</a>
</li>
<li>
<a href="/windows/desktop/shell/abm-setautohidebar">ABM_SETAUTOHIDEBAR</a>
</li>
<li>
<a href="/windows/desktop/shell/abm-getautohidebarex">ABM_GETAUTOHIDEBAREX</a>
</li>
<li>
<a href="/windows/desktop/shell/abm-setautohidebarex">ABM_SETAUTOHIDEBAREX</a>
</li>
<li>
<a href="/windows/desktop/shell/abm-querypos">ABM_QUERYPOS</a>
</li>
<li>
<a href="/windows/desktop/shell/abm-setpos">ABM_SETPOS</a>
</li>
</ul>


This member can be one of the following values.



#### ABE_BOTTOM

Bottom edge.



#### ABE_LEFT

Left edge.



#### ABE_RIGHT

Right edge.



#### ABE_TOP

Top edge.

### -field rc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure whose use varies depending on the message:
                    
                        

<ul>
<li>
<a href="/windows/desktop/shell/abm-gettaskbarpos">ABM_GETTASKBARPOS</a>, <a href="/windows/desktop/shell/abm-querypos">ABM_QUERYPOS</a>, <a href="/windows/desktop/shell/abm-setpos">ABM_SETPOS</a>: The bounding rectangle, in screen coordinates, of an appbar or the Windows taskbar.</li>
<li>
<a href="/windows/desktop/shell/abm-getautohidebarex">ABM_GETAUTOHIDEBAREX</a>, <a href="/windows/desktop/shell/abm-setautohidebarex">ABM_SETAUTOHIDEBAREX</a>: The monitor on which the operation is being performed. This information can be retrieved through the <a href="/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa">GetMonitorInfo</a> function.</li>
</ul>

### -field lParam

Type: <b>LPARAM</b>

A message-dependent value. This member is used with these messages:
                        
<ul>
<li>
<a href="/windows/desktop/shell/abm-setautohidebar">ABM_SETAUTOHIDEBAR</a>
</li>
<li>
<a href="/windows/desktop/shell/abm-setautohidebarex">ABM_SETAUTOHIDEBAREX</a>
</li>
<li>
<a href="/windows/desktop/shell/abm-setstate">ABM_SETSTATE</a>
</li>
</ul>


See the individual message pages for details.
