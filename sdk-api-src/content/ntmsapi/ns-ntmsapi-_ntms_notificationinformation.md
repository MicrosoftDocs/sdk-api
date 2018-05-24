---
UID: NS:ntmsapi._NTMS_NOTIFICATIONINFORMATION
title: "_NTMS_NOTIFICATIONINFORMATION"
author: windows-driver-content
description: The NTMS_NOTIFICATIONINFORMATION structure defines an object and operation that occurred in the RSM database.
old-location: fs\ntms_notificationinformation.htm
old-project: Rsm
ms.assetid: d9c6904b-260d-4598-9575-49c7d7b6e66d
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: "*LPNTMS_NOTIFICATIONINFORMATION, LPNTMS_NOTIFICATIONINFORMATION, LPNTMS_NOTIFICATIONINFORMATION structure pointer [Files], NTMS_NOTIFICATIONINFORMATION, NTMS_NOTIFICATIONINFORMATION structure [Files], NTMS_OBJ_DELETE, NTMS_OBJ_INSERT, NTMS_OBJ_UPDATE, _NTMS_NOTIFICATIONINFORMATION, _zaw_ntms_notificationinformation, base.ntms_notificationinformation, fs.ntms_notificationinformation, ntmsapi/LPNTMS_NOTIFICATIONINFORMATION, ntmsapi/NTMS_NOTIFICATIONINFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: NTMS_NOTIFICATIONINFORMATION, *LPNTMS_NOTIFICATIONINFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntmsapi.h
api_name:
-	NTMS_NOTIFICATIONINFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _NTMS_NOTIFICATIONINFORMATION structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_NOTIFICATIONINFORMATION</b> structure defines an object and operation that occurred in the RSM database.


## -struct-fields




### -field dwOperation

Operation that occurred on the object. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_OBJ_INSERT"></a><a id="ntms_obj_insert"></a><dl>
<dt><b>NTMS_OBJ_INSERT</b></dt>
</dl>
</td>
<td width="60%">
New object was inserted.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OBJ_DELETE"></a><a id="ntms_obj_delete"></a><dl>
<dt><b>NTMS_OBJ_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Object was deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OBJ_UPDATE"></a><a id="ntms_obj_update"></a><dl>
<dt><b>NTMS_OBJ_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Object was updated.

</td>
</tr>
</table>
 


### -field ObjectId

Object Identifier.


## -see-also




<a href="https://msdn.microsoft.com/ecb39bac-f062-4835-bbae-f9f643ffde9b">WaitForNtmsNotification</a>
 

 

