---
UID: NE:tapi3if.CALL_PRIVILEGE
title: CALL_PRIVILEGE
author: windows-driver-content
description: A CALL_PRIVILEGE member is returned by the ITCallInfo::get_Privilege method, and indicates when the current application owns or is monitoring the current call.
old-location: tapi3\call_privilege.htm
old-project: Tapi
ms.assetid: 8d2ab3d2-9531-40fc-910d-2bd81a075cc3
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: CALL_PRIVILEGE, CALL_PRIVILEGE enumeration [TAPI 2.2], CP_MONITOR, CP_OWNER, _tapi3_call_privilege, tapi3.call_privilege, tapi3if/CALL_PRIVILEGE, tapi3if/CP_MONITOR, tapi3if/CP_OWNER
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CALL_PRIVILEGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi3if.h
api_name:
-	CALL_PRIVILEGE
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CALL_PRIVILEGE enumeration


## -description


A 
<b>CALL_PRIVILEGE</b> member is returned by the 
<a href="https://msdn.microsoft.com/64a80fb6-b5bc-45c5-9f1d-a89ac95b9c53">ITCallInfo::get_Privilege</a> method, and indicates when the current application owns or is monitoring the current call.


## -enum-fields




### -field CP_OWNER

The application is the owner of the call.


### -field CP_MONITOR

The application is a monitor of the call.


## -see-also




<a href="https://msdn.microsoft.com/64a80fb6-b5bc-45c5-9f1d-a89ac95b9c53">ITCallInfo::get_Privilege</a>
 

 

