---
UID: NS:commctrl.tagTBSAVEPARAMSA
title: TBSAVEPARAMSA (commctrl.h)
description: Specifies the location in the registry where the TB_SAVERESTORE message stores and retrieves information about the state of a toolbar. (ANSI)
helpviewer_keywords: ["*LPTBSAVEPARAMSA","TBSAVEPARAMS","TBSAVEPARAMS structure [Windows Controls]","TBSAVEPARAMSA","TBSAVEPARAMSW","_win32_TBSAVEPARAMS","_win32_TBSAVEPARAMS_cpp","commctrl/TBSAVEPARAMS","commctrl/TBSAVEPARAMSA","commctrl/TBSAVEPARAMSW","controls.TBSAVEPARAMS","controls._win32_TBSAVEPARAMS"]
old-location: controls\TBSAVEPARAMS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbsaveparams.htm
ms.date: 12/05/2018
ms.keywords: '*LPTBSAVEPARAMSA, TBSAVEPARAMS, TBSAVEPARAMS structure [Windows Controls], TBSAVEPARAMSA, TBSAVEPARAMSW, _win32_TBSAVEPARAMS, _win32_TBSAVEPARAMS_cpp, commctrl/TBSAVEPARAMS, commctrl/TBSAVEPARAMSA, commctrl/TBSAVEPARAMSW, controls.TBSAVEPARAMS, controls._win32_TBSAVEPARAMS'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TBSAVEPARAMSW (Unicode) and TBSAVEPARAMSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TBSAVEPARAMSA, *LPTBSAVEPARAMSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTBSAVEPARAMSA
 - commctrl/tagTBSAVEPARAMSA
 - LPTBSAVEPARAMSA
 - commctrl/LPTBSAVEPARAMSA
 - TBSAVEPARAMSA
 - commctrl/TBSAVEPARAMSA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TBSAVEPARAMS
 - TBSAVEPARAMSA
 - TBSAVEPARAMSW
---

# TBSAVEPARAMSA structure


## -description

Specifies the location in the registry where the <a href="/windows/desktop/Controls/tb-saverestore">TB_SAVERESTORE</a> message stores and retrieves information about the state of a toolbar.

## -struct-fields

### -field hkr

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HKEY</a></b>

Handle to the registry key.

### -field pszSubKey

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

Subkey name.

### -field pszValueName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

Value name.

## -remarks

> [!NOTE]
> The commctrl.h header defines TBSAVEPARAMS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
