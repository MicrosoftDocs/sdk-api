---
UID: NF:winuser.SetWinEventHook
title: SetWinEventHook function (winuser.h)
description: Sets an event hook function for a range of events.
helpviewer_keywords: ["SetWinEventHook","SetWinEventHook function [Windows Accessibility]","WINEVENT_INCONTEXT","WINEVENT_OUTOFCONTEXT","WINEVENT_SKIPOWNPROCESS","WINEVENT_SKIPOWNTHREAD","_msaa_SetWinEventHook","msaa.setwineventhook","winauto.setwineventhook","winuser/SetWinEventHook"]
old-location: winauto\setwineventhook.htm
tech.root: WinAuto
ms.assetid: 090bda1b-0635-4aa3-ae33-3987b36e30b8
ms.date: 12/05/2018
ms.keywords: SetWinEventHook, SetWinEventHook function [Windows Accessibility], WINEVENT_INCONTEXT, WINEVENT_OUTOFCONTEXT, WINEVENT_SKIPOWNPROCESS, WINEVENT_SKIPOWNTHREAD, _msaa_SetWinEventHook, msaa.setwineventhook, winauto.setwineventhook, winuser/SetWinEventHook
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - SetWinEventHook
 - winuser/SetWinEventHook
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-winevent-ext-l1-1-0.dll
 - ext-ms-win-ntuser-server-l1-1-1.dll
 - ext-ms-win-ntuser-server-l1-1-0.dll
 - user32.dll
 - API-MS-Win-RTCore-NTUser-Winevent-l1-1-0.dll
 - minuser.dll
api_name:
 - SetWinEventHook
---

# SetWinEventHook function


## -description

Sets an event hook function for a range of events.

## -parameters

### -param eventMin [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the <a href="/windows/desktop/WinAuto/event-constants">event constant</a> for the lowest event value in the range of events that are handled by the hook function. This parameter can be set to <b>EVENT_MIN</b> to indicate the lowest possible event value.

### -param eventMax [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the event constant for the highest event value in the range of events that are handled by the hook function. This parameter can be  set to <a href="/windows/desktop/WinAuto/event-constants">EVENT_MAX</a> to indicate the highest possible event value.

### -param hmodWinEventProc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMODULE</a></b>

Handle to the DLL that contains the hook function at <i>lpfnWinEventProc</i>, if the WINEVENT_INCONTEXT flag is specified in the <i>dwFlags</i> parameter. If the hook function is not located in a DLL, or if the WINEVENT_OUTOFCONTEXT flag is specified, this parameter is <b>NULL</b>.

### -param pfnWinEventProc [in]

Type: <b>WINEVENTPROC</b>

Pointer to the event hook function. For more information about this function, see <a href="/windows/desktop/api/winuser/nc-winuser-wineventproc">WinEventProc</a>.

### -param idProcess [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the ID of the process from which the hook function receives events. Specify zero (0) to receive events from all processes on the current desktop.

### -param idThread [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the ID of the thread from which the hook function receives events. If this parameter is zero, the hook function is associated with all existing threads on the current desktop.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


Flag values that specify the location of the hook function and of the events to be skipped. The following flags are valid:
			 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINEVENT_INCONTEXT"></a><a id="winevent_incontext"></a><dl>
<dt><b>WINEVENT_INCONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The DLL that contains the callback function is mapped into the address space of the process that generates the event. With this flag, the system sends event notifications to the callback function as they occur. The hook function must be in a DLL when this flag is specified. This flag has no effect when both the calling process and the generating process are not 32-bit or 64-bit processes, or when the generating process is a console application. For more information, see <a href="/windows/desktop/WinAuto/in-context-hook-functions">In-Context Hook Functions</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINEVENT_OUTOFCONTEXT"></a><a id="winevent_outofcontext"></a><dl>
<dt><b>WINEVENT_OUTOFCONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The callback function is not mapped into the address space of the process that generates the event. Because the hook function is called across process boundaries, the system must queue events. Although this method is asynchronous, events are guaranteed to be in sequential order. For more information, see <a href="/windows/desktop/WinAuto/out-of-context-hook-functions">Out-of-Context Hook Functions</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINEVENT_SKIPOWNPROCESS"></a><a id="winevent_skipownprocess"></a><dl>
<dt><b>WINEVENT_SKIPOWNPROCESS</b></dt>
</dl>
</td>
<td width="60%">
Prevents this instance of the hook from receiving the events that are generated by threads in this process. This flag does not prevent threads from generating events.

</td>
</tr>
<tr>
<td width="40%"><a id="WINEVENT_SKIPOWNTHREAD"></a><a id="winevent_skipownthread"></a><dl>
<dt><b>WINEVENT_SKIPOWNTHREAD</b></dt>
</dl>
</td>
<td width="60%">
Prevents this instance of the hook from receiving the events that are generated by the thread that is registering this hook.

</td>
</tr>
</table>
 

The following flag combinations are valid:

<ul>
<li>WINEVENT_INCONTEXT | WINEVENT_SKIPOWNPROCESS</li>
<li>WINEVENT_INCONTEXT | WINEVENT_SKIPOWNTHREAD</li>
<li>WINEVENT_OUTOFCONTEXT | WINEVENT_SKIPOWNPROCESS</li>
<li>WINEVENT_OUTOFCONTEXT | WINEVENT_SKIPOWNTHREAD</li>
</ul>
Additionally, client applications can specify WINEVENT_INCONTEXT, or WINEVENT_OUTOFCONTEXT alone.

See Remarks section for information on Windows Store app development.

## -returns

Type: <b>HWINEVENTHOOK</b>

If successful, returns an <a href="/windows/desktop/WinAuto/hwineventhook">HWINEVENTHOOK</a> value that identifies this event hook instance. Applications save this return value to use it with the <a href="/windows/desktop/api/winuser/nf-winuser-unhookwinevent">UnhookWinEvent</a> function.

If unsuccessful, returns zero.

## -remarks

This function allows clients to specify which processes and threads they are interested in.

If the <i>idProcess</i> parameter is nonzero and <i>idThread</i> is zero, the hook function receives the specified events from all threads in that process. If the <i>idProcess</i> parameter is zero and <i>idThread</i> is nonzero, the hook function receives the specified events only from the thread specified by <i>idThread</i>. If both are zero, the hook function receives the specified events from all threads and processes.

Clients can call <b>SetWinEventHook</b> multiple times if they want to register additional hook functions or listen for additional events.

The client thread that calls <b>SetWinEventHook</b> must have a message loop in order to receive events.

When you use <b>SetWinEventHook</b> to set a callback in managed code, you should use the <a href="/dotnet/api/system.runtime.interopservices.gchandle">GCHandle</a> structure to avoid exceptions. This tells the garbage collector not to move the callback.

For out-of-context events, the event is delivered on the same thread that called <b>SetWinEventHook</b>. In some situations, even if you request WINEVENT_INCONTEXT events, the events will still be delivered out-of-context. These scenarios include events from console windows and events from processes that have a different bit-depth (64 bit versus 32 bits) than the caller. 



While a hook function processes an event, additional events may be triggered, which may cause the hook function to reenter before the processing for the original event is finished. The problem with reentrancy in hook functions is that events are completed out of sequence unless the hook function handles this situation. For more information, see <a href="/windows/desktop/WinAuto/guarding-against-reentrancy-in-hook-functions">Guarding Against Reentrancy</a>.

<b>Windows Store app development</b> If dwFlags is WINEVENT_INCONTEXT AND (idProcess = 0 | idThread = 0), then window hook DLLs are not loaded in-process for the Windows Store app processes and the Windows Runtime broker process unless they are installed by UIAccess processes (accessibility tools). The notification is delivered on the installer's thread.

This behavior is similar to what happens when there is an architecture mismatch between the hook DLL and the target application process, for example, when the hook DLL is 32-bit and the application process 64-bit. 


#### Examples

The following example code shows how a client application might listen for menu-start and menu-end events. For simplicity, the event handler just sends some information to the standard output.




```

// Global variable.
HWINEVENTHOOK g_hook;

// Initializes COM and sets up the event hook.
//
void InitializeMSAA()
{
    CoInitialize(NULL);
    g_hook = SetWinEventHook(
        EVENT_SYSTEM_MENUSTART, EVENT_SYSTEM_MENUEND,  // Range of events (4 to 5).
        NULL,                                          // Handle to DLL.
        HandleWinEvent,                                // The callback.
        0, 0,              // Process and thread IDs of interest (0 = all)
        WINEVENT_OUTOFCONTEXT | WINEVENT_SKIPOWNPROCESS); // Flags.
}

// Unhooks the event and shuts down COM.
//
void ShutdownMSAA()
{
    UnhookWinEvent(g_hook);
    CoUninitialize();
}

// Callback function that handles events.
//
void CALLBACK HandleWinEvent(HWINEVENTHOOK hook, DWORD event, HWND hwnd, 
                             LONG idObject, LONG idChild, 
                             DWORD dwEventThread, DWORD dwmsEventTime)
{
    IAccessible* pAcc = NULL;
    VARIANT varChild;
    HRESULT hr = AccessibleObjectFromEvent(hwnd, idObject, idChild, &pAcc, &varChild);  
    if ((hr == S_OK) && (pAcc != NULL))
    {
        BSTR bstrName;
        pAcc->get_accName(varChild, &bstrName);
        if (event == EVENT_SYSTEM_MENUSTART) 
        {
            printf("Begin: ");
        }
        else if (event == EVENT_SYSTEM_MENUEND)
        {
            printf("End:   ");
        }
        printf("%S\n", bstrName);
        SysFreeString(bstrName);
        pAcc->Release();
    }
}

```

## -see-also

<a href="/windows/desktop/WinAuto/registering-a-hook-function">Registering a Hook Function</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unhookwinevent">UnhookWinEvent</a>



<a href="/windows/desktop/api/winuser/nc-winuser-wineventproc">WinEventProc</a>