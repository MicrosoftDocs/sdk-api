---
UID: NF:vfw.MCIWndResume
title: MCIWndResume macro (vfw.h)
description: The MCIWndResume macro resumes playback or recording content from the paused mode. This macro restarts playback or recording from the current position in the content. You can use this macro or explicitly send the MCI_RESUME command.
helpviewer_keywords: ["MCIWndResume","MCIWndResume macro [Windows Multimedia]","_win32_MCIWndResume","multimedia.mciwndresume","vfw/MCIWndResume"]
old-location: multimedia\mciwndresume.htm
tech.root: Multimedia
ms.assetid: 08b0dc42-edf2-485b-8b00-164157117a32
ms.date: 07/01/2025
ms.keywords: MCIWndResume, MCIWndResume macro [Windows Multimedia], _win32_MCIWndResume, multimedia.mciwndresume, vfw/MCIWndResume
req.header: vfw.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCIWndResume
 - vfw/MCIWndResume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndResume
---

# MCIWndResume macro

## -syntax

```cpp
LONG MCIWndResume(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndResume</b> macro resumes playback or recording content from the paused mode. This macro restarts playback or recording from the current position in the content. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mci-resume">MCI_RESUME</a> command.

## -parameters

### -param hwnd

Handle of the MCIWnd window.
