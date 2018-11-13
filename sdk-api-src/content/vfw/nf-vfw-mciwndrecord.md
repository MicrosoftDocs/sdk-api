---
UID: NF:vfw.MCIWndRecord
title: MCIWndRecord macro
author: windows-sdk-content
description: The MCIWndRecord macro begins recording content using the MCI device. The recording process begins at the current position in the content and will overwrite existing data for the duration of the recording.
old-location: multimedia\mciwndrecord.htm
tech.root: Multimedia
ms.assetid: 9f68f258-6e7d-45f0-8b42-93a03d559c04
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: MCIWndRecord, MCIWndRecord macro [Windows Multimedia], _win32_MCIWndRecord, multimedia.mciwndrecord, vfw/MCIWndRecord
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MCIWndRecord macro


## -description



The <b>MCIWndRecord</b> macro begins recording content using the MCI device. The recording process begins at the current position in the content and will overwrite existing data for the duration of the recording.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


## -remarks



The function that an MCI device performs during recording depends on the characteristics of the device. An MCI device that uses files, such as a waveform-audio device, sends data to the file during recording. An MCI device that does not use files, such as a video-cassette recorder, receives and externally records data on another medium.



