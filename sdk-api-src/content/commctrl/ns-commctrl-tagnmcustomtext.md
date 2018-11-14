---
UID: NS:commctrl.tagNMCUSTOMTEXT
title: tagNMCUSTOMTEXT
author: windows-sdk-content
description: Contains information used with custom text notification.
old-location: controls\NMCUSTOMTEXT.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\structures\nmcustomtext.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPNMCUSTOMTEXT, LPNMCUSTOMTEXT, LPNMCUSTOMTEXT structure pointer [Windows Controls], NMCUSTOMTEXT, NMCUSTOMTEXT structure [Windows Controls], _shell_NMCUSTOMTEXT, _shell_NMCUSTOMTEXT_cpp, commctrl/LPNMCUSTOMTEXT, commctrl/NMCUSTOMTEXT, controls.NMCUSTOMTEXT, controls._shell_NMCUSTOMTEXT, tagNMCUSTOMTEXT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: commctrl.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMCUSTOMTEXT
product: Windows
targetos: Windows
req.typenames: NMCUSTOMTEXT, *LPNMCUSTOMTEXT
req.redist: 
---

# tagNMCUSTOMTEXT structure


## -description


Contains information used with custom text notification. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about this notification. 


### -field hDC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

The device context to draw to.


### -field lpString

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The string to draw.


### -field nCount

Type: <b>int</b>

Length of lpString.


### -field lpRect

Type: <b>LPRECT</b>

The rect to draw in.


### -field uFormat

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

One or more of the DT_* flags. For more information, see the description of the <i>uFormat</i> parameter of the <a href="https://msdn.microsoft.com/fe412280-d797-4abd-8a29-107a9cd96145">DrawText</a> function. This may be <b>NULL</b>.


### -field fLink

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Whether the text is a link.

