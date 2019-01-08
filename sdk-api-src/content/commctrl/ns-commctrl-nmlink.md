---
UID: NS:commctrl.tagNMLINK
title: NMLINK
author: windows-sdk-content
description: The NMLINK Contains notification information. Send this structure with the NM_CLICK or NM_RETURN messages.
old-location: controls\NMLINK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\syslink\structures\nmlink.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PNMLINK, NMLINK, NMLINK structure [Windows Controls], PNMLINK, PNMLINK structure pointer [Windows Controls], commctrl/NMLINK, commctrl/PNMLINK, controls.NMLINK, controls.inet_NMLINK_str, inet_NMLINK_str, inet_NMLINK_str_cpp"
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - NMLINK
product: Windows
targetos: Windows
req.typenames: NMLINK, *PNMLINK
req.redist: 
---

# NMLINK structure


## -description


The <b>NMLINK</b> Contains notification information. Send this structure with the <a href="https://msdn.microsoft.com/en-us/library/Bb760714(v=VS.85).aspx">NM_CLICK</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb775562(v=VS.85).aspx">NM_RETURN</a> messages.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about the notification.


### -field item

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb760710(v=VS.85).aspx">LITEM</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb760710(v=VS.85).aspx">LITEM</a> structure that contains information about the link item.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb760710(v=VS.85).aspx">LITEM</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb760714(v=VS.85).aspx">NM_CLICK (syslink)</a>



<b>Reference</b>
 

 

