---
UID: NS:commctrl.tagNMCUSTOMSPLITRECTINFO
title: tagNMCUSTOMSPLITRECTINFO
author: windows-sdk-content
description: Contains information about the two rectangles of a split button. Sent with the NM_GETCUSTOMSPLITRECT notification.
old-location: controls\NMCUSTOMSPLITRECTINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmcustomsplitrectinfo.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*LPNMCUSTOMSPLITRECTINFO, LPNMCUSTOMSPLITRECTINFO, LPNMCUSTOMSPLITRECTINFO structure pointer [Windows Controls], NMCUSTOMSPLITRECTINFO, NMCUSTOMSPLITRECTINFO structure [Windows Controls], _shell_NMCUSTOMSPLITRECTINFO, _shell_NMCUSTOMSPLITRECTINFO_cpp, commctrl/LPNMCUSTOMSPLITRECTINFO, commctrl/NMCUSTOMSPLITRECTINFO, controls.NMCUSTOMSPLITRECTINFO, controls._shell_NMCUSTOMSPLITRECTINFO, tagNMCUSTOMSPLITRECTINFO"
ms.prod: windows
ms.technology: windows-sdk
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
 - NMCUSTOMSPLITRECTINFO
product: Windows
targetos: Windows
req.typenames: NMCUSTOMSPLITRECTINFO, *LPNMCUSTOMSPLITRECTINFO
req.redist: 
---

# tagNMCUSTOMSPLITRECTINFO structure


## -description


Contains information about the two rectangles of a split button. Sent with the <a href="https://msdn.microsoft.com/ce72778d-3cca-46a4-9d05-40954a18681d">NM_GETCUSTOMSPLITRECT</a> notification.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about the notification. 


### -field rcClient

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that describes the client area the button occupies.


### -field rcButton

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that describes the rectangle that does not contain the drop-down arrow.


### -field rcSplit

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that describes the rectangle that contains the drop-down arrow.


## -remarks



This information is used to draw the button. The button must be of style <a href="Button_Styles.htm">BS_SPLITBUTTON</a> or <a href="Button_Styles.htm">BS_DEFSPLITBUTTON</a>



