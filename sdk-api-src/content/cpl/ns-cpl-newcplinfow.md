---
UID: NS:cpl.tagNEWCPLINFOW
title: NEWCPLINFOW (cpl.h)
description: Contains resource information and an application-defined value for a dialog box supported by a Control Panel application. (NEWCPLINFOW)
helpviewer_keywords: ["*LPNEWCPLINFOW","LPNEWCPLINFO","LPNEWCPLINFO structure pointer [Windows Shell]","NEWCPLINFO","NEWCPLINFO structure [Windows Shell]","NEWCPLINFOW","_win32_NEWCPLINFO","cpl/LPNEWCPLINFO","cpl/NEWCPLINFO","shell.NEWCPLINFO"]
old-location: shell\NEWCPLINFO.htm
tech.root: shell
ms.assetid: a68cd816-6b2c-4cff-9288-9c3758e3fdae
ms.date: 12/05/2018
ms.keywords: '*LPNEWCPLINFOW, LPNEWCPLINFO, LPNEWCPLINFO structure pointer [Windows Shell], NEWCPLINFO, NEWCPLINFO structure [Windows Shell], NEWCPLINFOW, _win32_NEWCPLINFO, cpl/LPNEWCPLINFO, cpl/NEWCPLINFO, shell.NEWCPLINFO'
req.header: cpl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NEWCPLINFOW, *LPNEWCPLINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNEWCPLINFOW
 - cpl/tagNEWCPLINFOW
 - LPNEWCPLINFOW
 - cpl/LPNEWCPLINFOW
 - NEWCPLINFOW
 - cpl/NEWCPLINFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cpl.h
api_name:
 - NEWCPLINFO
 - NEWCPLINFOW
---

## -description

Contains resource information and an application-defined value for a dialog box supported by a Control Panel application.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

The length of the structure, in bytes.

### -field dwFlags

Type: <b>DWORD</b>

This member is ignored.

### -field dwHelpContext

Type: <b>DWORD</b>

This member is ignored.

### -field lData

Type: <b>LONG_PTR</b>

A pointer to data defined by the application. When the Control Panel sends the <a href="/windows/desktop/shell/fa-associationarray">CPL_DBLCLK</a> and <a href="/windows/desktop/shell/library-functions-bumper">CPL_STOP</a> messages, it passes this value back to your application.

### -field hIcon

Type: <b>HICON</b>

The identifier of the icon that represents the dialog box. This icon is intended to be displayed by the application that controls the Control Panel application.

### -field szName

Type: <b>TCHAR[32]</b>

A null-terminated string that contains the dialog box name. The name is intended to be displayed below the icon.

### -field szInfo

Type: <b>TCHAR[64]</b>

A null-terminated string containing the dialog box description. The description is intended to be displayed when the icon for the dialog box is selected.

### -field szHelpFile

Type: <b>TCHAR[128]</b>

This member is ignored.

## -remarks

The <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc">CPlApplet</a> function of the Control Panel application returns this information to the Control Panel in response to a <a href="/windows/desktop/shell/glossary">CPL_NEWINQUIRE</a> message.

> [!NOTE]
> The cpl.h header defines NEWCPLINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/cpl/ns-cpl-cplinfo">CPLINFO</a>
