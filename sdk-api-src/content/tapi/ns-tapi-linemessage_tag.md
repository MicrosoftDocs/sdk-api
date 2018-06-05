---
UID: NS:tapi.linemessage_tag
title: linemessage_tag
author: windows-sdk-content
description: The LINEMESSAGE structure contains parameter values specifying a change in status of the line the application currently has open. The lineGetMessage function returns the LINEMESSAGE structure.
old-location: tapi2\linemessage_str.htm
old-project: Tapi
ms.assetid: 1d184948-4ba2-4c8c-8771-d1aea6c4f565
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPLINEMESSAGE, LINEMESSAGE, LINEMESSAGE structure [TAPI 2.2], LPLINEMESSAGE, LPLINEMESSAGE structure pointer [TAPI 2.2], _tapi2_linemessage_str, linemessage_tag, tapi/LINEMESSAGE, tapi/LPLINEMESSAGE, tapi2.linemessage_str"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: LINEMESSAGE, *LPLINEMESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	LINEMESSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# linemessage_tag structure


## -description


The 
<b>LINEMESSAGE</b> structure contains parameter values specifying a change in status of the line the application currently has open. The 
<a href="https://msdn.microsoft.com/ed6df53e-b01d-40bc-8676-b0f7e0eacfd1">lineGetMessage</a> function returns the 
<b>LINEMESSAGE</b> structure.


## -struct-fields




### -field hDevice

Handle to either a line device or a call. The nature of this handle (line handle or call handle) can be determined by the context provided by <i>dwMessageID</i>.


### -field dwMessageID

Line or call device message.


### -field dwCallbackInstance

Instance data passed back to the application, which was specified by the application in the <i>dwCallBackInstance</i> parameter of 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>. This <b>DWORD</b> is not interpreted by TAPI.


### -field dwParam1

Parameter for the message.


### -field dwParam2

Parameter for the message.


### -field dwParam3

Parameter for the message.


## -remarks



For information about parameter values passed in this structure, see 
<a href="https://msdn.microsoft.com/dc11134e-6c20-426e-834e-508bf855e5da">Line Device Messages</a>.




## -see-also




<a href="https://msdn.microsoft.com/ed6df53e-b01d-40bc-8676-b0f7e0eacfd1">lineGetMessage</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>
 

 

