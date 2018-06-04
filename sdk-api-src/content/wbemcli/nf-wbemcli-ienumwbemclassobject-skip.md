---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IEnumWbemClassObject::Skip


## -description


You can use the 
<b>IEnumWbemClassObject::Skip</b> method to move the current position in an enumeration ahead by a specified number of objects. Also, this affects subsequent calls to 
<a href="https://msdn.microsoft.com/1ff82982-a2d7-4618-8488-9e4b7628012d">NextAsync</a>, but it does not affect pending deliveries begun with 
<b>NextAsync</b>.


## -parameters




### -param lTimeout




### -param nCount






#### - UCount [in]

Number of objects to skip. If this parameter is greater than the number of objects left to enumerate, then this call skips to the end of the enumeration and <b>WBEM_S_FALSE</b> is returned.


#### - lTimeOut [in]

Maximum amount of time in milliseconds that the call to 
<b>Skip</b> blocks before returning. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the operation succeeds. If 
<b>Skip</b> cannot complete the operation before the <i>lTimeout</i> value expires, the call returns <b>WBEM_S_TIMEDOUT</b>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.



