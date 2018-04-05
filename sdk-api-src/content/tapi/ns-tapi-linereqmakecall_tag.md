---
UID: NS:tapi.linereqmakecall_tag
title: linereqmakecall_tag
author: windows-driver-content
description: The LINEREQMAKECALL structure describes a request initiated by a call to the lineGetRequest function.
old-location: tapi2\linereqmakecall_str.htm
old-project: Tapi
ms.assetid: de4e51af-ea1c-41aa-b5a9-9fa628e18d9d
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPLINEREQMAKECALL, LINEREQMAKECALL, LINEREQMAKECALL structure [TAPI 2.2], LPLINEREQMAKECALL, LPLINEREQMAKECALL structure pointer [TAPI 2.2], _tapi2_linereqmakecall_str, linereqmakecall_tag, tapi/LINEREQMAKECALL, tapi/LPLINEREQMAKECALL, tapi2.linereqmakecall_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tapi.h
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
req.typenames: LINEREQMAKECALL, *LPLINEREQMAKECALL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	LINEREQMAKECALL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# linereqmakecall_tag structure


## -description


The 
<b>LINEREQMAKECALL</b> structure describes a request initiated by a call to the 
<a href="https://msdn.microsoft.com/c72ed61f-abbe-4a6d-9f8d-95afbd5dfb04">lineGetRequest</a> function.


## -struct-fields




### -field szDestAddress

<b>Null</b>-terminated destination address of the make-call request. The address can use the canonical address format or the dialable address format. The maximum length of the address is TAPIMAXDESTADDRESSSIZE characters, which includes the <b>NULL</b> terminator. Longer strings are truncated.


### -field szAppName

<b>Null</b>-terminated user-friendly application name or filename of the application that originated the request. The maximum length of the address is TAPIMAXAPPNAMESIZE characters, which includes the <b>NULL</b> terminator.


### -field szCalledParty

<b>Null</b>-terminated user-friendly called-party name. The maximum length of the called-party information is TAPIMAXCALLEDPARTYSIZE characters, which includes the <b>NULL</b> terminator.


### -field szComment

<b>Null</b>-terminated comment about the call request. The maximum length of the comment string is TAPIMAXCOMMENTSIZE characters, which includes the <b>NULL</b> terminator.


## -remarks



This structure may not be extended.

The <b>szDestAddress</b> member contains the address of the remote party; the other members are useful for logging purposes. An application must use this structure to interpret the request buffer it received from 
<a href="https://msdn.microsoft.com/c72ed61f-abbe-4a6d-9f8d-95afbd5dfb04">lineGetRequest</a> with the LINEREQUESTMODE_MAKECALL request mode.




## -see-also




<a href="https://msdn.microsoft.com/c72ed61f-abbe-4a6d-9f8d-95afbd5dfb04">lineGetRequest</a>
 

 

