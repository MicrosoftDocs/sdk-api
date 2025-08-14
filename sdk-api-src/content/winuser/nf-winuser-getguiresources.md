---
UID: NF:winuser.GetGuiResources
title: GetGuiResources (winuser.h)
old-location: base\getguiresources.htm
tech.root: backup
ms.assetid: 55fbb7e8-79b4-4011-b522-25ea5a928b86
ms.date: 11/4/2019
ms.keywords: GR_GDIOBJECTS, GR_GDIOBJECTS_PEAK, GR_USEROBJECTS, GR_USEROBJECTS_PEAK, GetGuiResources, GetGuiResources function, _win32_getguiresources, base.getguiresources, winuser/GetGuiResources
targetos: Windows
description: Retrieves the count of handles to graphical user interface (GUI) objects in use by the specified process.
helpviewer_keywords: ["GR_GDIOBJECTS","GR_GDIOBJECTS_PEAK","GR_USEROBJECTS","GR_USEROBJECTS_PEAK","GetGuiResources","GetGuiResources function","_win32_getguiresources","base.getguiresources","winuser/GetGuiResources"]
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: User32.dll
req.header: winuser.h
req.idl: 
req.include-header: windows.h
req.irql: 
req.kmdf-ver: 
req.lib: User32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - GetGuiResources
 - winuser/GetGuiResources
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetGuiResources
dev_langs:
 - c++
req.apiset: ext-ms-win-ntuser-misc-l1-1-0 (introduced in Windows 8)
---

## -description

Retrieves the count of handles to graphical user interface (GUI) objects in use by the specified process.

## -parameters

### -param hProcess [in]

A handle to the process. The handle must refer to a process in the current session, and must have the **PROCESS_QUERY_LIMITED_INFORMATION** access right (see [Process security and access rights](/windows/win32/procthread/process-security-and-access-rights)).

If this parameter is the special value **GR_GLOBAL**, then the resource usage is reported across all processes in the current session.

**Windows Server 2008, Windows Vista, Windows Server 2003, and Windows XP:** The **GR_GLOBAL** value is not supported until Windows 7 and Windows Server 2008 R2.

**Windows Server 2003 and Windows XP:** The handle must have the **PROCESS_QUERY_INFORMATION** access right.

### -param uiFlags [in]

The GUI object type. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GR_GDIOBJECTS"></a><a id="gr_gdiobjects"></a><dl>
<dt><b>GR_GDIOBJECTS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Return the count of GDI objects.

</td>
</tr>
<tr>
<td width="40%"><a id="GR_GDIOBJECTS_PEAK"></a><a id="gr_gdiobjects_peak"></a><dl>
<dt><b>GR_GDIOBJECTS_PEAK</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Return the peak count of GDI objects.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows 7 and Windows Server 2008 R2.

</td>
</tr>
<tr>
<td width="40%"><a id="GR_USEROBJECTS"></a><a id="gr_userobjects"></a><dl>
<dt><b>GR_USEROBJECTS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Return the count of USER objects.

</td>
</tr>
<tr>
<td width="40%"><a id="GR_USEROBJECTS_PEAK"></a><a id="gr_userobjects_peak"></a><dl>
<dt><b>GR_USEROBJECTS_PEAK</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Return the peak count of USER objects.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows 7 and Windows Server 2008 R2.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the count of handles to GUI objects in use by the process. If no GUI objects are in use, the return value is zero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A process without a graphical user interface does not use GUI resources, therefore, 
<b>GetGuiResources</b> will return zero.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
