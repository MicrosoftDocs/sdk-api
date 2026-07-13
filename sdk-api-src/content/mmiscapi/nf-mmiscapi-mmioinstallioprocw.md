---
UID: NF:mmiscapi.mmioInstallIOProcW
title: mmioInstallIOProcW function (mmiscapi.h)
description: The mmioInstallIOProcW (Unicode) function installs or removes a custom I/O procedure and locates an installed I/O procedure, using its corresponding code.
helpviewer_keywords: ["_win32_mmioInstallIOProc", "mmioInstallIOProc", "mmioInstallIOProc function [Windows Multimedia]", "mmioInstallIOProcW", "multimedia.mmioinstallioproc"]
old-location: multimedia\mmioinstallioproc.htm
tech.root: Multimedia
ms.assetid: 235b5014-ad6e-4b9e-a063-99022cbcdb5d
ms.date: 08/02/2022
ms.keywords: _win32_mmioInstallIOProc, mmioInstallIOProc, mmioInstallIOProc function [Windows Multimedia], mmioInstallIOProcA, mmioInstallIOProcW, mmsystem/mmioInstallIOProc, mmsystem/mmioInstallIOProcA, mmsystem/mmioInstallIOProcW, multimedia.mmioinstallioproc
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: mmioInstallIOProcW (Unicode) and mmioInstallIOProcA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mmioInstallIOProcW
 - mmiscapi/mmioInstallIOProcW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-misc-l1-1-0.dll
 - winmmbase.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
api_name:
 - mmioInstallIOProc
 - mmioInstallIOProcA
 - mmioInstallIOProcW
---

# mmioInstallIOProcW function


## -description

The <b>mmioInstallIOProc</b> function installs or removes a custom I/O procedure. This function also locates an installed I/O procedure, using its corresponding four-character code.

## -parameters

### -param fccIOProc

Four-character code identifying the I/O procedure to install, remove, or locate. All characters in this code should be uppercase.

### -param pIOProc

Pointer to the I/O procedure to install. To remove or locate an I/O procedure, set this parameter to <b>NULL</b>. For more information about the I/O procedure, see <a href="/previous-versions/dd757332(v=vs.85)">MMIOProc</a>.

### -param dwFlags

Flag indicating whether the I/O procedure is being installed, removed, or located. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MMIO_FINDPROC</td>
<td>Searches for the specified I/O procedure.</td>
</tr>
<tr>
<td>MMIO_GLOBALPROC</td>
<td>This flag is a modifier to the MMIO_INSTALLPROC flag and indicates the I/O procedure should be installed for global use. This flag is ignored if MMIO_FINDPROC or MMIO_REMOVEPROC is specified.</td>
</tr>
<tr>
<td>MMIO_INSTALLPROC</td>
<td>Installs the specified I/O procedure.</td>
</tr>
<tr>
<td>MMIO_REMOVEPROC</td>
<td>Removes the specified I/O procedure.</td>
</tr>
</table>

## -returns

Returns the address of the I/O procedure installed, removed, or located. Returns <b>NULL</b> if there is an error.

## -remarks

> [!NOTE]
> The mmiscapi.h header defines mmioInstallIOProc as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
