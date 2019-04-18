---
UID: NF:shellapi.SHAppBarMessage
title: SHAppBarMessage function (shellapi.h)
author: windows-sdk-content
description: Sends an appbar message to the system.
old-location: shell\SHAppBarMessage.htm
tech.root: shell
ms.assetid: 173d6eff-b33b-4d7d-bedd-5ebfb1e45954
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ABM_ACTIVATE, ABM_GETAUTOHIDEBAR, ABM_GETAUTOHIDEBAREX, ABM_GETSTATE, ABM_GETTASKBARPOS, ABM_NEW, ABM_QUERYPOS, ABM_REMOVE, ABM_SETAUTOHIDEBAR, ABM_SETAUTOHIDEBAREX, ABM_SETPOS, ABM_SETSTATE, ABM_WINDOWPOSCHANGED, SHAppBarMessage, SHAppBarMessage function [Windows Shell], _win32_SHAppBarMessage, shell.SHAppBarMessage, shellapi/SHAppBarMessage
ms.topic: function
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHAppBarMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHAppBarMessage function


## -description


Sends an appbar message to the system.


## -parameters




### -param dwMessage [in]

Type: <b>DWORD</b>

Appbar message value to send. This parameter can be one of the following values.



#### ABM_NEW (0x00000000)

Registers a new appbar and specifies the message identifier that the system should use to send notification messages to the appbar.



#### ABM_REMOVE (0x00000001)

Unregisters an appbar, removing the bar from the system's internal list.



#### ABM_QUERYPOS (0x00000002)

Requests a size and screen position for an appbar.



#### ABM_SETPOS (0x00000003)

Sets the size and screen position of an appbar.



#### ABM_GETSTATE (0x00000004)

Retrieves the autohide and always-on-top states of the Windows taskbar.



#### ABM_GETTASKBARPOS (0x00000005)

Retrieves the bounding rectangle of the Windows taskbar. Note that this applies only to the system taskbar. Other objects, particularly toolbars supplied with third-party software, also can be present. As a result, some of the screen area not covered by the Windows taskbar might not be visible to the user. To retrieve the area of the screen not covered by both the taskbar and other app bars—the working area available to your application—, use the <a href="https://msdn.microsoft.com/025a89c2-4bbd-4c8b-8367-3735fb5b872a">GetMonitorInfo</a> function.



#### ABM_ACTIVATE (0x00000006)

Notifies the system to activate or deactivate an appbar. The <b>lParam</b> member of the <a href="https://msdn.microsoft.com/cf86fe15-4beb-49b7-b73e-2ad61cedc3f8">APPBARDATA</a> pointed to by <i>pData</i> is set to <b>TRUE</b> to activate or <b>FALSE</b> to deactivate.



#### ABM_GETAUTOHIDEBAR (0x00000007)

Retrieves the handle to the autohide appbar associated with a particular edge of the screen.



#### ABM_SETAUTOHIDEBAR (0x00000008)

Registers or unregisters an autohide appbar for an edge of the screen.



#### ABM_WINDOWPOSCHANGED (0x00000009)

Notifies the system when an appbar's position has changed.



#### ABM_SETSTATE (0x0000000A)

<b>Windows XP and later:</b> Sets the state of the appbar's autohide and always-on-top attributes.



#### ABM_GETAUTOHIDEBAREX (0x0000000B)

<b>Windows XP and later:</b> Retrieves the handle to the autohide appbar associated with a particular edge of a particular monitor.



#### ABM_SETAUTOHIDEBAREX (0x0000000C)

<b>Windows XP and later:</b> Registers or unregisters an autohide appbar for an edge of a particular monitor.


### -param pData [in, out]

Type: <b>PAPPBARDATA</b>

A pointer to an <a href="https://msdn.microsoft.com/cf86fe15-4beb-49b7-b73e-2ad61cedc3f8">APPBARDATA</a> structure. The content of the structure on entry and on exit depends on the value set in the <i>dwMessage</i> parameter. See the individual message pages for specifics.


## -returns



Type: <b>UINT_PTR</b>

This function returns a message-dependent value. For more information, see the Windows SDK documentation for the specific appbar message sent. Links to those documents are given in the See Also section.




## -see-also




<a href="https://msdn.microsoft.com/16011302-7c2d-4c34-9953-51cceb96e4b3">ABM_ACTIVATE</a>



<a href="https://msdn.microsoft.com/545dd1d9-8cbb-4ff3-b871-4908ecac56db">ABM_GETAUTOHIDEBAR</a>



<a href="https://msdn.microsoft.com/538EA230-06DF-4441-A6AA-9DD613521BE1">ABM_GETAUTOHIDEBAREX</a>



<a href="https://msdn.microsoft.com/18e16752-16be-492b-a4fa-c951e18dc86c">ABM_GETSTATE</a>



<a href="https://msdn.microsoft.com/8072bb2d-05e6-4baa-a7f4-1377b94fdd45">ABM_GETTASKBARPOS</a>



<a href="https://msdn.microsoft.com/1da9db13-6fdc-44b3-9985-de32d572675a">ABM_NEW</a>



<a href="https://msdn.microsoft.com/061a30fb-a68a-464e-ad8c-0bda672b57d9">ABM_QUERYPOS</a>



<a href="https://msdn.microsoft.com/3da73a52-3dbb-4133-a9bd-86540e1c4154">ABM_REMOVE</a>



<a href="https://msdn.microsoft.com/0cbd6c9c-e83f-41f8-91ed-81afaa24f524">ABM_SETAUTOHIDEBAR</a>



<a href="https://msdn.microsoft.com/C437727C-3FF6-4598-9D81-A39FCC2EF1C4">ABM_SETAUTOHIDEBAREX</a>



<a href="https://msdn.microsoft.com/b3c56278-b9a2-4e08-bf98-7b3e4c8bd082">ABM_SETPOS</a>



<a href="https://msdn.microsoft.com/a60e156d-19ef-49b9-83fc-138d1a2169f2">ABM_SETSTATE</a>



<a href="https://msdn.microsoft.com/8ca51f5f-b6cf-4f2c-98f4-69c992679320">ABM_WINDOWPOSCHANGED</a>
 

 

