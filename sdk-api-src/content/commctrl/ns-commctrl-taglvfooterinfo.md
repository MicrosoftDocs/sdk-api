---
UID: NS:commctrl.tagLVFOOTERINFO
title: tagLVFOOTERINFO
author: windows-sdk-content
description: Contains information on a footer in a list-view control.
old-location: controls\LVFOOTERINFO.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvfooterinfo.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*LPLVFOOTERINFO, LPLVFOOTERINFO, LPLVFOOTERINFO structure pointer [Windows Controls], LVFOOTERINFO, LVFOOTERINFO structure [Windows Controls], _shell_LVFOOTERINFO, _shell_LVFOOTERINFO_cpp, commctrl/LPLVFOOTERINFO, commctrl/LVFOOTERINFO, controls.LVFOOTERINFO, controls._shell_LVFOOTERINFO, tagLVFOOTERINFO"
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
 - LVFOOTERINFO
product: Windows
targetos: Windows
req.typenames: LVFOOTERINFO, *LPLVFOOTERINFO
req.redist: 
---

# tagLVFOOTERINFO structure


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



This structure is used with the <a href="https://msdn.microsoft.com/941d86d8-96f4-4eeb-83b2-c00b279a2cc2">ListView_GetFooterInfo</a> macro and the <a href="https://msdn.microsoft.com/5734e151-50c0-46df-8f2c-220c4910a590">LVM_GETFOOTERINFO</a> message.

The creation of footers in list-view controls is currently not supported.



