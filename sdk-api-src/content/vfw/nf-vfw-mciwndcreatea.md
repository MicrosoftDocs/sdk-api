---
UID: NF:vfw.MCIWndCreateA
title: MCIWndCreateA function (vfw.h)
description: The MCIWndCreate function registers the MCIWnd window class and creates an MCIWnd window for using MCI services. MCIWndCreate can also open an MCI device or file (such as an AVI file) and associate it with the MCIWnd window. (ANSI)
helpviewer_keywords: ["MCIWndCreateA", "vfw/MCIWndCreateA"]
old-location: multimedia\mciwndcreate.htm
tech.root: Multimedia
ms.assetid: 7a4a22e1-6b04-4d46-8427-738181769f5b
ms.date: 12/05/2018
ms.keywords: MCIWndCreate, MCIWndCreate function [Windows Multimedia], MCIWndCreateA, MCIWndCreateW, _win32_MCIWndCreate, multimedia.mciwndcreate, vfw/MCIWndCreate, vfw/MCIWndCreateA, vfw/MCIWndCreateW
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MCIWndCreateW (Unicode) and MCIWndCreateA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCIWndCreateA
 - vfw/MCIWndCreateA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - MCIWndCreate
 - MCIWndCreateA
 - MCIWndCreateW
---

# MCIWndCreateA function


## -description

The <b>MCIWndCreate</b> function registers the MCIWnd window class and creates an MCIWnd window for using MCI services. <b>MCIWndCreate</b> can also open an MCI device or file (such as an AVI file) and associate it with the MCIWnd window.

## -parameters

### -param hwndParent

Handle to the parent window.

### -param hInstance

Handle to the module instance to associate with the MCIWnd window.

### -param dwStyle

Flags defining the window style. In addition to specifying the window styles used with the <a href="/windows/win32/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function, you can specify the following styles to use with MCIWnd windows.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MCIWNDF_NOAUTOSIZEWINDOW</td>
<td>Will not change the dimensions of an MCIWnd window when the image size changes.</td>
</tr>
<tr>
<td>MCIWNDF_NOAUTOSIZEMOVIE</td>
<td>Will not change the dimensions of the destination rectangle when an MCIWnd window size changes.</td>
</tr>
<tr>
<td>MCIWNDF_NOERRORDLG</td>
<td>Inhibits display of MCI errors to users.</td>
</tr>
<tr>
<td>MCIWNDF_NOMENU</td>
<td>Hides the Menu button from view on the toolbar and prohibits users from accessing its pop-up menu.</td>
</tr>
<tr>
<td>MCIWNDF_NOOPEN</td>
<td>Hides the open and close commands from the MCIWnd menu and prohibits users from accessing these choices in the pop-up menu.</td>
</tr>
<tr>
<td>MCIWNDF_NOPLAYBAR</td>
<td>Hides the toolbar from view and prohibits users from accessing it.</td>
</tr>
<tr>
<td>MCIWNDF_NOTIFYANSI</td>
<td>Causes MCIWnd to use an ANSI string instead of a Unicode string when notifying the parent window of device mode changes. This flag is used in combination with MCIWNDF_NOTIFYMODE.</td>
</tr>
<tr>
<td>MCIWNDF_NOTIFYMODE</td>
<td>Causes MCIWnd to notify the parent window with an <a href="/windows/desktop/Multimedia/mciwndm-notifymode">MCIWNDM_NOTIFYMODE</a> message whenever the device changes operating modes. The <i>lParam</i> parameter of this message identifies the new mode, such as MCI_MODE_STOP.</td>
</tr>
<tr>
<td>MCIWNDF_NOTIFYPOS</td>
<td>Causes MCIWnd to notify the parent window with an <a href="/windows/desktop/Multimedia/mciwndm-notifypos">MCIWNDM_NOTIFYPOS</a> message whenever a change in the playback or record position within the content occurs. The <i>lParam</i> parameter of this message contains the new position in the content.</td>
</tr>
<tr>
<td>MCIWNDF_NOTIFYMEDIA</td>
<td>Causes MCIWnd to notify the parent window with an <a href="/windows/desktop/Multimedia/mciwndm-notifymedia">MCIWNDM_NOTIFYMEDIA</a> message whenever a new device is used or a data file is opened or closed. The <i>lParam</i> parameter of this message contains a pointer to the new file name.</td>
</tr>
<tr>
<td>MCIWNDF_NOTIFYSIZE</td>
<td>Causes MCIWnd to notify the parent window when the MCIWnd window size changes.</td>
</tr>
<tr>
<td>MCIWNDF_NOTIFYERROR</td>
<td>Causes MCIWnd to notify the parent window when an MCI error occurs.</td>
</tr>
<tr>
<td>MCIWNDF_NOTIFYALL</td>
<td>Causes all MCIWNDF window notification styles to be used.</td>
</tr>
<tr>
<td>MCIWNDF_RECORD</td>
<td>Adds a Record button to the toolbar and adds a new file command to the menu if the MCI device has recording capability.</td>
</tr>
<tr>
<td>MCIWNDF_SHOWALL</td>
<td>Causes all MCIWNDF_SHOW styles to be used.</td>
</tr>
<tr>
<td>MCIWNDF_SHOWMODE</td>
<td>Displays the current mode of the MCI device in the window title bar. For a list of device modes, see the <a href="/windows/desktop/api/vfw/nf-vfw-mciwndgetmode">MCIWndGetMode</a> macro.</td>
</tr>
<tr>
<td>MCIWNDF_SHOWNAME</td>
<td>Displays the name of the open MCI device or data file in the MCIWnd window title bar.</td>
</tr>
<tr>
<td>MCIWNDF_SHOWPOS</td>
<td>Displays the current position within the content of the MCI device in the window title bar.</td>
</tr>
</table>

### -param szFile

Null-terminated string indicating the name of an MCI device or data file to open.

## -returns

Returns the handle to an MCI window if successful or zero otherwise.

## -remarks

Default window styles for a child window are WS_CHILD, WS_BORDER, and WS_VISIBLE. <b>MCIWndCreate</b> assumes a child window when a non-<b>NULL</b> handle of a parent window is specified.

Default window styles for a parent window are WS_OVERLAPPEDWINDOW and WS_VISIBLE. <b>MCIWndCreate</b> assumes a parent window when a <b>NULL</b> handle of a parent window is specified.

Use the window handle returned by this function for the window handle in the MCIWnd macros. If your application uses this function, it does not need to use the <a href="/windows/desktop/api/vfw/nf-vfw-mciwndregisterclass">MCIWndRegisterClass</a> function.





> [!NOTE]
> The vfw.h header defines MCIWndCreate as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-notifymedia">MCIWNDM_NOTIFYMEDIA</a>



<a href="/windows/desktop/Multimedia/mciwndm-notifymode">MCIWNDM_NOTIFYMODE</a>



<a href="/windows/desktop/Multimedia/mciwndm-notifypos">MCIWNDM_NOTIFYPOS</a>



<a href="/windows/desktop/api/vfw/nf-vfw-mciwndgetmode">MCIWndGetMode</a>



<a href="/windows/desktop/api/vfw/nf-vfw-mciwndregisterclass">MCIWndRegisterClass</a>
