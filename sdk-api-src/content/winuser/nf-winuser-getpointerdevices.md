---
UID: NF:winuser.GetPointerDevices
title: GetPointerDevices function (winuser.h)
description: Gets information about the pointer devices attached to the system.
helpviewer_keywords: ["GetPointerDevices","GetPointerDevices function","input_pointerdevice.getpointerdevices","unifiedinputstack.getpointerdevices","winuser/GetPointerDevices"]
old-location: input_pointerdevice\getpointerdevices.htm
tech.root: controls
ms.assetid: 91FD5EBA-EDD7-4D7D-ABF3-3CE2461417B0
ms.date: 12/05/2018
ms.keywords: GetPointerDevices, GetPointerDevices function, input_pointerdevice.getpointerdevices, unifiedinputstack.getpointerdevices, winuser/GetPointerDevices
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - GetPointerDevices
 - winuser/GetPointerDevices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-wmpointermin-l1-1-0.dll
 - api-ms-win-rtcore-ntuser-wmpointer-l1-2-0.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - GetPointerDevices
req.apiset: ext-ms-win-rtcore-ntuser-wmpointer-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# GetPointerDevices function


## -description

Gets information about the pointer devices attached to the system.

## -parameters

### -param deviceCount [in, out]

If <i>pointerDevices</i> is NULL, <i>deviceCount</i> returns the total number of attached pointer devices. Otherwise, <i>deviceCount</i> specifies the number of <a href="/windows/desktop/api/winuser/ns-winuser-pointer_device_info">POINTER_DEVICE_INFO</a> structures pointed to by <i>pointerDevices</i>.

### -param pointerDevices [out, optional]

Array of <a href="/windows/desktop/api/winuser/ns-winuser-pointer_device_info">POINTER_DEVICE_INFO</a> structures for the pointer devices attached to the system. If NULL, the total number of attached pointer devices is returned in <i>deviceCount</i>.

## -returns

If this function succeeds, it returns TRUE.
 
Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

Windows 8 supports the following:

<ul>
<li>256 contacts per pointer device.</li>
<li>2560 total contacts per system session, regardless of the number of attached devices. For example, 10 pointer devices with 256 contacts each, 20 pointer devices with 128 contacts each, and so on.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/input_pointerdevice/functions">Functions</a>
