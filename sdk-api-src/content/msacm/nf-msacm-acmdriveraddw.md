---
UID: NF:msacm.acmDriverAddW
title: acmDriverAddW function (msacm.h)
description: The acmDriverAddW (Unicode) function (msacm.h) adds a driver to the list of available ACM drivers. (acmDriverAddW)
helpviewer_keywords: ["_win32_acmDriverAdd", "acmDriverAdd", "acmDriverAdd function [Windows Multimedia]", "acmDriverAddW", "msacm/acmDriverAdd", "msacm/acmDriverAddW", "multimedia.acmdriveradd"]
old-location: multimedia\acmdriveradd.htm
tech.root: Multimedia
ms.assetid: f037cab8-a1f4-487f-ab0a-11e11993b007
ms.date: 08/02/2022
ms.keywords: _win32_acmDriverAdd, acmDriverAdd, acmDriverAdd function [Windows Multimedia], acmDriverAddA, acmDriverAddW, msacm/acmDriverAdd, msacm/acmDriverAddA, msacm/acmDriverAddW, multimedia.acmdriveradd
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmDriverAddW (Unicode) and acmDriverAddA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - acmDriverAddW
 - msacm/acmDriverAddW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmDriverAdd
 - acmDriverAddA
 - acmDriverAddW
---

# acmDriverAddW function


## -description

The <b>acmDriverAdd</b> function adds a driver to the list of available ACM drivers. The driver type and location are dependent on the flags used to add ACM drivers. After a driver is successfully added, the driver entry function will receive ACM driver messages.

## -parameters

### -param phadid

Pointer to the buffer that receives a handle identifying the installed driver. This handle is used to identify the driver in calls to other ACM functions.

### -param hinstModule

Handle to the instance of the module whose executable or dynamic-link library (DLL) contains the driver entry function.

### -param lParam

Driver function address or a notification window handle, depending on the <i>fdwAdd</i> flags.

### -param dwPriority

Window message to send for notification broadcasts. This parameter is used only with the ACM_DRIVERADDF_NOTIFYHWND flag. All other flags require this member to be set to zero.

### -param fdwAdd

Flags for adding ACM drivers. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACM_DRIVERADDF_FUNCTION</td>
<td>The <i>lParam</i> parameter is a driver function address conforming to the <a href="/windows/desktop/api/msacm/nc-msacm-acmdriverproc">acmDriverProc</a> prototype. The function may reside in either an executable or DLL file.</td>
</tr>
<tr>
<td>ACM_DRIVERADDF_GLOBAL</td>
<td>Provided for compatibility with 16-bit applications. For the Win32 API, ACM drivers added by the <b>acmDriverAdd</b> function can be used only by the application that added the driver. This is true whether or not ACM_DRIVERADDF_GLOBAL is specified. For more information, see <a href="/windows/desktop/Multimedia/adding-drivers-within-an-application">Adding Drivers Within an Application</a>.</td>
</tr>
<tr>
<td>ACM_DRIVERADDF_LOCAL</td>
<td>The ACM automatically gives a local driver higher priority than a global driver when searching for a driver to satisfy a function call. For more information, see <a href="/windows/desktop/Multimedia/adding-drivers-within-an-application">Adding Drivers Within an Application</a>.</td>
</tr>
<tr>
<td>ACM_DRIVERADDF_NAME</td>
<td>The <i>lParam</i> parameter is a registry value name in HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Drivers32. The value identifies a DLL that implements an ACM codec. Applications can use this flag if new registry entries are created after the application has already started using the ACM.</td>
</tr>
<tr>
<td>ACM_DRIVERADDF_NOTIFYHWND</td>
<td>The <i>lParam</i> parameter is a handle of a notification window that receives messages when changes to global driver priorities and states are made. The window message to receive is defined by the application and must be passed in <i>dwPriority</i>. The <i>wParam</i> and <i>lParam</i> parameters passed with the window message are reserved for future use and should be ignored. ACM_DRIVERADDF_GLOBAL cannot be specified in conjunction with this flag. For more information about driver priorities, see the description for the <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverpriority">acmDriverPriority</a> function.</td>
</tr>
</table>

## -returns

Returns zero if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALFLAG</b></dt>
</dl>
</td>
<td width="60%">
At least one flag is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to allocate resources.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>

## -remarks

> [!NOTE]
> The msacm.h header defines acmDriverAdd as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
