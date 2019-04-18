---
UID: NS:commctrl.tagLVFOOTERINFO
title: LVFOOTERINFO (commctrl.h)
author: windows-sdk-content
description: Contains information on a footer in a list-view control.
old-location: controls\LVFOOTERINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvfooterinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLVFOOTERINFO, LPLVFOOTERINFO, LPLVFOOTERINFO structure pointer [Windows Controls], LVFOOTERINFO, LVFOOTERINFO structure [Windows Controls], _shell_LVFOOTERINFO, _shell_LVFOOTERINFO_cpp, commctrl/LPLVFOOTERINFO, commctrl/LVFOOTERINFO, controls.LVFOOTERINFO, controls._shell_LVFOOTERINFO"
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
 - LVFOOTERINFO
product: Windows
targetos: Windows
req.typenames: LVFOOTERINFO, *LPLVFOOTERINFO
req.redist: 
ms.custom: 19H1
---

# LVFOOTERINFO structure


## -description


Contains information on a footer in a list-view control.


## -struct-fields




### -field mask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Set of flags that specify which members of this structure contain data to be set or which members are being requested. Currently, this value must be LVFF_ITEMCOUNT, for the <b>cItems</b> member.


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Not supported. Must be set to zero.


### -field cchTextMax

Type: <b>int</b>

Not supported. Must be set to zero.


### -field cItems

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of items in the footer. When this structure is used to get information, this member will be set by the message receiver.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb761268(v=VS.85).aspx">ListView_GetFooterInfo</a> macro and the <a href="https://msdn.microsoft.com/en-us/library/Bb774927(v=VS.85).aspx">LVM_GETFOOTERINFO</a> message.

The creation of footers in list-view controls is currently not supported.



