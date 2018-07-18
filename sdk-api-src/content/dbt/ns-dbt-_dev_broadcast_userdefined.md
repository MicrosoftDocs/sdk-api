---
UID: NS:dbt._DEV_BROADCAST_USERDEFINED
title: "_DEV_BROADCAST_USERDEFINED"
author: windows-sdk-content
description: Contains the user-defined event and optional data associated with the DBT_USERDEFINED device event.
old-location: base\_dev_broadcast_userdefined_str.htm
old-project: devio
ms.assetid: e90fbce2-cae7-4e78-b6f5-82b200390cb7
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "_DEV_BROADCAST_USERDEFINED, _DEV_BROADCAST_USERDEFINED structure, _win32__dev_broadcast_userdefined_str, base._dev_broadcast_userdefined_str, dbt/_DEV_BROADCAST_USERDEFINED"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dbt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dbt.h
api_name:
 - _DEV_BROADCAST_USERDEFINED
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DEV_BROADCAST_USERDEFINED structure


## -description


Contains the user-defined event and optional data associated with the 
<a href="https://msdn.microsoft.com/b42feda9-5fe7-4e54-aad9-28c61d2f29b6">DBT_USERDEFINED</a> device event.


## -struct-fields




### -field dbud_dbh

Information about the device affected by a 
<a href="https://msdn.microsoft.com/b64a3983-ee75-4199-9778-1e5b7cec59e4">WM_DEVICECHANGE</a> message as specified by the 
<a href="https://msdn.microsoft.com/4fc81fcb-b9fe-4016-b639-a43845af2c5f">DEV_BROADCAST_HDR</a> structure. Because 
<b>_DEV_BROADCAST_USERDEFINED</b> is variable length, the <b>dbch_size</b> member of the <b>dbud_dbh</b> structure must be the size in bytes of the entire structure, including the variable length portion.


### -field dbud_szName

A pointer to a case-sensitive, null-terminated string that names the message. The string must consist of the vendor name, a backslash, followed by arbitrary user-defined null-terminated text.


## -remarks



Because this structure contains variable length fields, use it as a template for creating a pointer to a user-defined structure. Note that the structure must not contain pointers. The following example shows such a user-defined structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define NAME_LENGTH 32 
#define USER_LENGTH 50 
 
typedef struct tagWIDGET_WARE_DEV_BROADCAST_USERDEFINED
{
    struct _DEV_BROADCAST_HDR DBHeader; 
    char   szName[NAME_LENGTH];
    BYTE   UserDefined[USER_LENGTH]; 
} WIDGET_WARE_DEV_BROADCAST_USERDEFINED;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b42feda9-5fe7-4e54-aad9-28c61d2f29b6">DBT_USERDEFINED</a>



<a href="https://msdn.microsoft.com/4fc81fcb-b9fe-4016-b639-a43845af2c5f">DEV_BROADCAST_HDR</a>



<a href="https://msdn.microsoft.com/b64a3983-ee75-4199-9778-1e5b7cec59e4">WM_DEVICECHANGE</a>
 

 

