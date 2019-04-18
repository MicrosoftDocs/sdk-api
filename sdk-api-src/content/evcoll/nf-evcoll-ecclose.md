---
UID: NF:evcoll.EcClose
title: EcClose function (evcoll.h)
author: windows-sdk-content
description: Closes a handle received from other Event Collector functions.
old-location: wec\ecclose.htm
tech.root: WEC
ms.assetid: a2dc71e3-7580-4484-9a08-4e3ee2139921
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EcClose, EcClose function, evcoll/EcClose, wec.ecclose, wes.ecclose
ms.topic: function
req.header: evcoll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wecapi.dll
api_name:
 - EcClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EcClose function


## -description


The <b>EcClose</b> function closes a handle received from other Event Collector functions. Any handle returned by an event collector management API call must be closed using this call when the user is finished with the handle. The handle becomes invalid when this function is successfully called.


## -parameters




### -param Object [in]

A valid open handle returned from an event collector management API call.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

