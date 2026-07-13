---
UID: NS:processthreadsapi._STARTUPINFOW
title: STARTUPINFOW (processthreadsapi.h)
description: Specifies the window station, desktop, standard handles, and appearance of the main window for a process at creation time. (Unicode)
helpviewer_keywords: ["*LPSTARTUPINFOW","LPSTARTUPINFO","LPSTARTUPINFO structure pointer","STARTF_FORCEOFFFEEDBACK","STARTF_FORCEONFEEDBACK","STARTF_PREVENTPINNING","STARTF_RUNFULLSCREEN","STARTF_TITLEISAPPID","STARTF_TITLEISLINKNAME","STARTF_UNTRUSTEDSOURCE","STARTF_USECOUNTCHARS","STARTF_USEFILLATTRIBUTE","STARTF_USEHOTKEY","STARTF_USEPOSITION","STARTF_USESHOWWINDOW","STARTF_USESIZE","STARTF_USESTDHANDLES","STARTUPINFO","STARTUPINFO structure","STARTUPINFOA","STARTUPINFOW","_win32_startupinfo_str","base.startupinfo_str","processthreadsapi/LPSTARTUPINFO","processthreadsapi/STARTUPINFO","processthreadsapi/STARTUPINFOA","processthreadsapi/STARTUPINFOW","winbase/LPSTARTUPINFO","winbase/STARTUPINFO","winbase/STARTUPINFOA","winbase/STARTUPINFOW"]
old-location: base\startupinfo_str.htm
tech.root: processthreadsapi
ms.assetid: cf4b795c-52c1-4573-8328-99ee13f68bb3
ms.date: 12/05/2018
ms.keywords: '*LPSTARTUPINFOW, LPSTARTUPINFO, LPSTARTUPINFO structure pointer, STARTF_FORCEOFFFEEDBACK, STARTF_FORCEONFEEDBACK, STARTF_PREVENTPINNING, STARTF_RUNFULLSCREEN, STARTF_TITLEISAPPID, STARTF_TITLEISLINKNAME, STARTF_UNTRUSTEDSOURCE, STARTF_USECOUNTCHARS, STARTF_USEFILLATTRIBUTE, STARTF_USEHOTKEY, STARTF_USEPOSITION, STARTF_USESHOWWINDOW, STARTF_USESIZE, STARTF_USESTDHANDLES, STARTUPINFO, STARTUPINFO structure, STARTUPINFOA, STARTUPINFOW, _win32_startupinfo_str, base.startupinfo_str, processthreadsapi/LPSTARTUPINFO, processthreadsapi/STARTUPINFO, processthreadsapi/STARTUPINFOA, processthreadsapi/STARTUPINFOW, winbase/LPSTARTUPINFO, winbase/STARTUPINFO, winbase/STARTUPINFOA, winbase/STARTUPINFOW'
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: STARTUPINFOW (Unicode) and STARTUPINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STARTUPINFOW, *LPSTARTUPINFOW
req.redist: 
ms.custom: snippet-project
f1_keywords:
 - _STARTUPINFOW
 - processthreadsapi/_STARTUPINFOW
 - LPSTARTUPINFOW
 - processthreadsapi/LPSTARTUPINFOW
 - STARTUPINFOW
 - processthreadsapi/STARTUPINFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
 - processthreadsapi.h
api_name:
 - STARTUPINFO
 - STARTUPINFOA
 - STARTUPINFOW
---

# STARTUPINFOW structure


## -description

Specifies the window station, desktop, standard handles, and appearance of the main window for a process at creation time.

## -struct-fields

### -field cb

The size of the structure, in bytes.

### -field lpReserved

Reserved; must be NULL.

### -field lpDesktop

The name of the desktop, or the name of both the desktop and window station for this process. A backslash in the string indicates that the string includes both the desktop and window station names. 

For more information, see [Thread Connection to a Desktop](/windows/desktop/winstation/thread-connection-to-a-desktop).

### -field lpTitle

For console processes, this is the title displayed in the title bar if a new console window is created. If NULL, the name of the executable file is used as the window title instead. This parameter must be NULL for GUI or console processes that do not create a new console window.

### -field dwX

If <b>dwFlags</b> specifies STARTF_USEPOSITION, this member is the x offset of the upper left corner of a window if a new window is created, in pixels. Otherwise, this member is ignored. 




The offset is from the upper left corner of the screen. For GUI processes, the specified position is used the first time the new process calls <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> to create an overlapped window if the <i>x</i> parameter of <b>CreateWindow</b> is CW_USEDEFAULT.

### -field dwY

If <b>dwFlags</b> specifies STARTF_USEPOSITION, this member is the y offset of the upper left corner of a window if a new window is created, in pixels. Otherwise, this member is ignored. 




The offset is from the upper left corner of the screen. For GUI processes, the specified position is used the first time the new process calls <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> to create an overlapped window if the <i>y</i> parameter of <b>CreateWindow</b> is CW_USEDEFAULT.

### -field dwXSize

If <b>dwFlags</b> specifies STARTF_USESIZE, this member is the width of the window if a new window is created, in pixels. Otherwise, this member is ignored. 




For GUI processes, this is used only the first time the new process calls <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> to create an overlapped window if the <i>nWidth</i> parameter of <b>CreateWindow</b> is CW_USEDEFAULT.

### -field dwYSize

If <b>dwFlags</b> specifies STARTF_USESIZE, this member is the height of the window if a new window is created, in pixels. Otherwise, this member is ignored. 




For GUI processes, this is used only the first time the new process calls <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> to create an overlapped window if the <i>nHeight</i> parameter of <b>CreateWindow</b> is CW_USEDEFAULT.

### -field dwXCountChars

 If <b>dwFlags</b> specifies STARTF_USECOUNTCHARS, if a new console window is created in a console process, this member specifies the screen buffer width, in character columns. Otherwise, this member is ignored.

### -field dwYCountChars

 If <b>dwFlags</b> specifies STARTF_USECOUNTCHARS, if a new console window is created in a console process, this member specifies the screen buffer height, in character rows. Otherwise, this member is ignored.

### -field dwFillAttribute

If <b>dwFlags</b> specifies STARTF_USEFILLATTRIBUTE, this member is the initial text and background colors if a new console window is created in a console application. Otherwise, this member is ignored. 




This value can be any combination of the following values: FOREGROUND_BLUE, FOREGROUND_GREEN, FOREGROUND_RED, FOREGROUND_INTENSITY, BACKGROUND_BLUE, BACKGROUND_GREEN, BACKGROUND_RED, and BACKGROUND_INTENSITY. For example, the following combination of values produces red text on a white background:

<code>FOREGROUND_RED| BACKGROUND_RED| BACKGROUND_GREEN| BACKGROUND_BLUE</code>

### -field dwFlags

A bitfield that determines whether certain 
<b>STARTUPINFO</b> members are used when the process creates a window. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STARTF_FORCEONFEEDBACK"></a><a id="startf_forceonfeedback"></a><dl>
<dt><b>STARTF_FORCEONFEEDBACK</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Indicates that the cursor is in feedback mode for two seconds after 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> is called. The Working in Background cursor is displayed (see the Pointers tab in the Mouse control panel utility). 




If during those two seconds the process makes the first GUI call, the system gives five more seconds to the process. If during those five seconds the process shows a window, the system gives five more seconds to the process to finish drawing the window.

The system turns the feedback cursor off after the first call to 
<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a>, regardless of whether the process is drawing.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_FORCEOFFFEEDBACK"></a><a id="startf_forceofffeedback"></a><dl>
<dt><b>STARTF_FORCEOFFFEEDBACK</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Indicates that the feedback cursor is forced off while the process is starting. The Normal Select cursor is displayed.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_PREVENTPINNING"></a><a id="startf_preventpinning"></a><dl>
<dt><b>STARTF_PREVENTPINNING</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Indicates that any windows created by the process cannot be pinned on the taskbar.

This flag must be combined with STARTF_TITLEISAPPID.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_RUNFULLSCREEN"></a><a id="startf_runfullscreen"></a><dl>
<dt><b>STARTF_RUNFULLSCREEN</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
 Indicates that the process should be run in full-screen mode, rather than in windowed mode. 




This flag is only valid for console applications running on an x86 computer.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_TITLEISAPPID"></a><a id="startf_titleisappid"></a><dl>
<dt><b>STARTF_TITLEISAPPID</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The <b>lpTitle</b> member contains an AppUserModelID. This identifier controls how the taskbar and <b>Start</b> menu present the application, and enables it to be associated with the correct shortcuts and Jump Lists. Generally, applications will use the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid">SetCurrentProcessExplicitAppUserModelID</a> and <b>GetCurrentProcessExplicitAppUserModelID</b> functions instead of setting this flag. For more information, see <a href="/windows/desktop/shell/appids">Application User Model IDs</a>.

If STARTF_PREVENTPINNING is used, application windows cannot be pinned on the taskbar. The use of any AppUserModelID-related window properties by the application overrides this setting for that window only.

This flag cannot be used with STARTF_TITLEISLINKNAME.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_TITLEISLINKNAME"></a><a id="startf_titleislinkname"></a><dl>
<dt><b>STARTF_TITLEISLINKNAME</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The <b>lpTitle</b> member contains the path of the shortcut file (.lnk) that the user invoked to start this process. This is typically set by the shell when a .lnk file pointing to the launched application is invoked.  Most applications will not need to set this value.

This flag cannot be used with STARTF_TITLEISAPPID.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_UNTRUSTEDSOURCE"></a><a id="startf_untrustedsource"></a><dl>
<dt><b>STARTF_UNTRUSTEDSOURCE</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The command line came from an untrusted source. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="STARTF_USECOUNTCHARS"></a><a id="startf_usecountchars"></a><dl>
<dt><b>STARTF_USECOUNTCHARS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
 The <b>dwXCountChars</b> and <b>dwYCountChars</b> members contain additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_USEFILLATTRIBUTE"></a><a id="startf_usefillattribute"></a><dl>
<dt><b>STARTF_USEFILLATTRIBUTE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The <b>dwFillAttribute</b> member contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_USEHOTKEY"></a><a id="startf_usehotkey"></a><dl>
<dt><b>STARTF_USEHOTKEY</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The <b>hStdInput</b> member contains additional information. 

This flag cannot be used with <b>STARTF_USESTDHANDLES</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_USEPOSITION"></a><a id="startf_useposition"></a><dl>
<dt><b>STARTF_USEPOSITION</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The <b>dwX</b> and <b>dwY</b> members contain additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_USESHOWWINDOW"></a><a id="startf_useshowwindow"></a><dl>
<dt><b>STARTF_USESHOWWINDOW</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <b>wShowWindow</b> member contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_USESIZE"></a><a id="startf_usesize"></a><dl>
<dt><b>STARTF_USESIZE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <b>dwXSize</b> and <b>dwYSize</b> members contain additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="STARTF_USESTDHANDLES"></a><a id="startf_usestdhandles"></a><dl>
<dt><b>STARTF_USESTDHANDLES</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The <b>hStdInput</b>, <b>hStdOutput</b>, and <b>hStdError</b> members contain additional information.  



							

If this flag is specified when calling one of the process creation functions, the handles must be inheritable and the 
function's <i>bInheritHandles</i> parameter must be set to TRUE. For more information, see 
<a href="/windows/desktop/SysInfo/handle-inheritance">Handle Inheritance</a>.

If this flag is specified when calling the [GetStartupInfo](./nf-processthreadsapi-getstartupinfow.md) function, these members are either the handle value specified during process creation or INVALID_HANDLE_VALUE.

Handles must be closed with 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> when they are no longer needed.

This flag cannot be used with <b>STARTF_USEHOTKEY</b>.

</td>
</tr>
</table>

### -field wShowWindow

If <b>dwFlags</b> specifies STARTF_USESHOWWINDOW, this member can be any of the values that can be specified in the <i>nCmdShow</i> parameter for the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function, except for SW_SHOWDEFAULT. Otherwise, this member is ignored. 




For GUI processes, the first time 
<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> is called, its <i>nCmdShow</i> parameter is ignored <b>wShowWindow</b> specifies the default value. In subsequent calls to <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>, the <b>wShowWindow</b> member is used if the <i>nCmdShow</i> parameter of <b>ShowWindow</b> is set to SW_SHOWDEFAULT.

### -field cbReserved2

Reserved for use by the C Run-time; must be zero.

### -field lpReserved2

Reserved for use by the C Run-time; must be NULL.

### -field hStdInput

If <b>dwFlags</b> specifies STARTF_USESTDHANDLES, this member is the standard input handle for the process. If STARTF_USESTDHANDLES is not specified, the default for standard input is the keyboard buffer.

If <b>dwFlags</b> specifies STARTF_USEHOTKEY, this member specifies a hotkey value that is sent as the <i>wParam</i> parameter of a <a href="/windows/win32/inputdev/wm-sethotkey">WM_SETHOTKEY</a> message to the first  eligible top-level window created by the application that owns the process. If the window is created with the WS_POPUP window style, it is not eligible unless the WS_EX_APPWINDOW extended window style is also set. For more information, see <a href="/windows/win32/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>.  

Otherwise, this member is ignored.

### -field hStdOutput

If <b>dwFlags</b> specifies STARTF_USESTDHANDLES, this member is the standard output handle for the process. Otherwise, this member is ignored and the default for standard output is the console window's buffer.

If a process is launched from the taskbar or jump list, the system sets <b>hStdOutput</b> to a handle to the monitor that contains the taskbar or jump list used to launch the process. For more information, see Remarks.<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>This behavior was introduced in Windows 8 and Windows Server 2012.

### -field hStdError

If <b>dwFlags</b> specifies STARTF_USESTDHANDLES, this member is the standard error handle for the process. Otherwise, this member is ignored and the default for standard error is the console window's buffer.

## -remarks

For graphical user interface (GUI) processes, this information affects the first window created by the 
<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> function and shown by the 
<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function. For console processes, this information affects the console window if a new console is created for the process. A process can use the 
[GetStartupInfo](./nf-processthreadsapi-getstartupinfow.md) function to retrieve the 
<b>STARTUPINFO</b> structure specified when the process was created.

If a GUI process is being started and neither STARTF_FORCEONFEEDBACK or STARTF_FORCEOFFFEEDBACK is specified, the process feedback cursor is used. A GUI process is one whose subsystem is specified as "windows."

If a process is launched from the taskbar or jump list, the system sets [GetStartupInfo](./nf-processthreadsapi-getstartupinfow.md) to retrieve the <b>STARTUPINFO</b> structure and check that <b>hStdOutput</b> is set. If so, use <a href="/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa">GetMonitorInfo</a> to check whether <b>hStdOutput</b> is a valid monitor handle (HMONITOR). The process can then use the handle to position its windows.

If the <b>STARTF_UNTRUSTEDSOURCE</b> flag is specified, the application should be aware that the command line is untrusted. If this flag is set, applications should disable potentially dangerous features such as macros, downloaded content, and automatic printing. This flag is optional. Applications that call <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> are encouraged to set this flag when launching a program with untrusted command line arguments (e.g. those provided by web content) so that the newly created process can apply appropriate policy.

The <b>STARTF_UNTRUSTEDSOURCE</b> flag is supported starting in Windows Vista, but it is not defined in the SDK header files prior to the Windows 10 SDK. To use the flag in versions prior to Windows 10, you can define it manually in your program.


#### Examples

The following code example shows the use of **StartUpInfoW**.

```cpp
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _tmain( int argc, TCHAR *argv[] )
{
    STARTUPINFO si;
    PROCESS_INFORMATION pi;

    ZeroMemory( &si, sizeof(si) );
    si.cb = sizeof(si);
    ZeroMemory( &pi, sizeof(pi) );

    if( argc != 2 )
    {
        printf("Usage: %s [cmdline]\n", argv[0]);
        return;
    }

    // Start the child process. 
    if( !CreateProcess( NULL,   // No module name (use command line)
        argv[1],        // Command line
        NULL,           // Process handle not inheritable
        NULL,           // Thread handle not inheritable
        FALSE,          // Set handle inheritance to FALSE
        0,              // No creation flags
        NULL,           // Use parent's environment block
        NULL,           // Use parent's starting directory 
        &si,            // Pointer to STARTUPINFO structure
        &pi )           // Pointer to PROCESS_INFORMATION structure
    ) 
    {
        printf( "CreateProcess failed (%d).\n", GetLastError() );
        return;
    }

    // Wait until child process exits.
    WaitForSingleObject( pi.hProcess, INFINITE );

    // Close process and thread handles. 
    CloseHandle( pi.hProcess );
    CloseHandle( pi.hThread );
}
```

For more information about this example, see 
<a href="/windows/desktop/ProcThread/creating-processes">Creating Processes</a>.

<div class="code"></div>




> [!NOTE]
> The processthreadsapi.h header defines STARTUPINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createprocesswithlogonw">CreateProcessWithLogonW</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createprocesswithtokenw">CreateProcessWithTokenW</a>



[GetStartupInfo](./nf-processthreadsapi-getstartupinfow.md)
