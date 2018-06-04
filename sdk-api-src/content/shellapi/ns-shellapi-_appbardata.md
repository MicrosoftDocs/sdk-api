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

# _AppBarData structure


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

An application-defined message identifier. The application uses the specified identifier for notification messages that it sends to the appbar identified by the <b>hWnd</b> member. This member is used when sending the <a href="https://msdn.microsoft.com/1da9db13-6fdc-44b3-9985-de32d572675a">ABM_NEW</a> message.


### -field uEdge

Type: <b>UINT</b>

A value that specifies an edge of the screen. This member is used when sending one of these messages:
                        
                            <ul>
<li>
<a href="https://msdn.microsoft.com/545dd1d9-8cbb-4ff3-b871-4908ecac56db">ABM_GETAUTOHIDEBAR</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0cbd6c9c-e83f-41f8-91ed-81afaa24f524">ABM_SETAUTOHIDEBAR</a>
</li>
<li>
<a href="https://msdn.microsoft.com/538EA230-06DF-4441-A6AA-9DD613521BE1">ABM_GETAUTOHIDEBAREX</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C437727C-3FF6-4598-9D81-A39FCC2EF1C4">ABM_SETAUTOHIDEBAREX</a>
</li>
<li>
<a href="https://msdn.microsoft.com/061a30fb-a68a-464e-ad8c-0bda672b57d9">ABM_QUERYPOS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b3c56278-b9a2-4e08-bf98-7b3e4c8bd082">ABM_SETPOS</a>
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

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure whose use varies depending on the message:
                    
                        

<ul>
<li>
<a href="https://msdn.microsoft.com/8072bb2d-05e6-4baa-a7f4-1377b94fdd45">ABM_GETTASKBARPOS</a>, <a href="https://msdn.microsoft.com/061a30fb-a68a-464e-ad8c-0bda672b57d9">ABM_QUERYPOS</a>, <a href="https://msdn.microsoft.com/b3c56278-b9a2-4e08-bf98-7b3e4c8bd082">ABM_SETPOS</a>: The bounding rectangle, in screen coordinates, of an appbar or the Windows taskbar.</li>
<li>
<a href="https://msdn.microsoft.com/538EA230-06DF-4441-A6AA-9DD613521BE1">ABM_GETAUTOHIDEBAREX</a>, <a href="https://msdn.microsoft.com/C437727C-3FF6-4598-9D81-A39FCC2EF1C4">ABM_SETAUTOHIDEBAREX</a>: The monitor on which the operation is being performed. This information can be retrieved through the <a href="https://msdn.microsoft.com/025a89c2-4bbd-4c8b-8367-3735fb5b872a">GetMonitorInfo</a> function.</li>
</ul>

### -field lParam

Type: <b>LPARAM</b>

A message-dependent value. This member is used with these messages:
                        
                            <ul>
<li>
<a href="https://msdn.microsoft.com/0cbd6c9c-e83f-41f8-91ed-81afaa24f524">ABM_SETAUTOHIDEBAR</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C437727C-3FF6-4598-9D81-A39FCC2EF1C4">ABM_SETAUTOHIDEBAREX</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a60e156d-19ef-49b9-83fc-138d1a2169f2">ABM_SETSTATE</a>
</li>
</ul>


See the individual message pages for details.

