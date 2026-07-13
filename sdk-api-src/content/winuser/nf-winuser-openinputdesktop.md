---
UID: NF:winuser.OpenInputDesktop
title: OpenInputDesktop function (winuser.h)
description: Opens the desktop that receives user input.
helpviewer_keywords: ["DF_ALLOWOTHERACCOUNTHOOK","OpenInputDesktop","OpenInputDesktop function [Windows Stations and Desktops]","base.openinputdesktop","winstation.openinputdesktop","winuser/OpenInputDesktop"]
old-location: winstation\openinputdesktop.htm
tech.root: winstation
ms.assetid: 023d421e-bf32-4e08-b5b3-b7b2ca6c4e00
ms.date: 12/05/2018
ms.keywords: DF_ALLOWOTHERACCOUNTHOOK, OpenInputDesktop, OpenInputDesktop function [Windows Stations and Desktops], base.openinputdesktop, winstation.openinputdesktop, winuser/OpenInputDesktop
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OpenInputDesktop
 - winuser/OpenInputDesktop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-winstamin-l1-1-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-1.dll
 - api-ms-win-rtcore-ntuser-windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - OpenInputDesktop
req.apiset: ext-ms-win-ntuser-windowstation-l1-1-1 (introduced in Windows 8.1)
---

# OpenInputDesktop function


## -description

Opens the desktop that receives user input.

## -parameters

### -param dwFlags [in]

This parameter can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DF_ALLOWOTHERACCOUNTHOOK"></a><a id="df_allowotheraccounthook"></a><dl>
<dt><b>DF_ALLOWOTHERACCOUNTHOOK</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Allows processes running in other accounts on the desktop to set hooks in this process.

</td>
</tr>
</table>

### -param fInherit [in]

If this value is <b>TRUE</b>, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.

### -param dwDesiredAccess [in]

The access to the desktop. For a list of access rights, see 
<a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktop Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is a handle to the desktop that receives user input. When you are finished using the handle, call the 
<a href="/windows/desktop/api/winuser/nf-winuser-closedesktop">CloseDesktop</a> function to close it.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The calling process must have an associated window station, either assigned by the system when the process is created, or set by 
the <a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a> function. The window station associated with the calling process must be capable of receiving input.

If the calling process is running in a disconnected session, the function returns a handle to the desktop that  becomes active when the user restores the connection.

An application can use the 
<a href="/windows/desktop/api/winuser/nf-winuser-switchdesktop">SwitchDesktop</a> function to change the input desktop.

If the <i>dwDesiredAccess</i> parameter specifies the <b>READ_CONTROL</b>, <b>WRITE_DAC</b>, or <b>WRITE_OWNER</b> standard access rights, you must also request the <b>DESKTOP_READOBJECTS</b> and <b>DESKTOP_WRITEOBJECTS</b> access rights.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-closedesktop">CloseDesktop</a>



<a href="/windows/desktop/winstation/desktops">Desktops</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-switchdesktop">SwitchDesktop</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
