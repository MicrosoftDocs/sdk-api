---
UID: NS:winuser.tagAUDIODESCRIPTION
title: AUDIODESCRIPTION (winuser.h)
description: Contains information associated with audio descriptions. This structure is used with the SystemParametersInfo function when the SPI_GETAUDIODESCRIPTION or SPI_SETAUDIODESCRIPTION action value is specified.
helpviewer_keywords: ["*LPAUDIODESCRIPTION","AUDIODESCRIPTION","AUDIODESCRIPTION structure [Windows and Messages]","LPAUDIODESCRIPTION","LPAUDIODESCRIPTION structure pointer [Windows and Messages]","audiodescription_cpp","base.audiodescription","tagAUDIODESCRIPTION","winmsg.audiodescription","winui.audiodescription","winuser/AUDIODESCRIPTION","winuser/LPAUDIODESCRIPTION"]
old-location: winmsg\audiodescription.htm
tech.root: winmsg
ms.assetid: 20eb48da-cd2b-4af8-b3a7-5ee3f39b1387
ms.date: 12/05/2018
ms.keywords: '*LPAUDIODESCRIPTION, AUDIODESCRIPTION, AUDIODESCRIPTION structure [Windows and Messages], LPAUDIODESCRIPTION, LPAUDIODESCRIPTION structure pointer [Windows and Messages], audiodescription_cpp, base.audiodescription, tagAUDIODESCRIPTION, winmsg.audiodescription, winui.audiodescription, winuser/AUDIODESCRIPTION, winuser/LPAUDIODESCRIPTION'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: AUDIODESCRIPTION, *LPAUDIODESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAUDIODESCRIPTION
 - winuser/tagAUDIODESCRIPTION
 - LPAUDIODESCRIPTION
 - winuser/LPAUDIODESCRIPTION
 - AUDIODESCRIPTION
 - winuser/AUDIODESCRIPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - AUDIODESCRIPTION
---

# AUDIODESCRIPTION structure


## -description

Contains information associated with audio descriptions. This structure is used with the 
<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function when the SPI_GETAUDIODESCRIPTION or SPI_SETAUDIODESCRIPTION action value is specified.

## -struct-fields

### -field cbSize

The size of the structure, in bytes. The caller must set this member to <code>sizeof(AUDIODESCRIPTION)</code>.

### -field Enabled

If this member is <b>TRUE</b>, audio descriptions are enabled; Otherwise, this member is <b>FALSE</b>.

### -field Locale

The locale identifier (LCID) of the language for the audio description. For more information, see 
       <a href="/windows/desktop/Intl/locales-and-languages">Locales and Languages</a>.

## -remarks

To compile an application that uses this structure, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>