---
UID: NC:fwpmu.FWPM_CONNECTION_CALLBACK0
title: FWPM_CONNECTION_CALLBACK0
author: windows-driver-content
description: Is used to add custom behavior to the connection object subscription process.
old-location: fwp\fwpm_connection_callback0.htm
old-project: FWP
ms.assetid: 92aac379-6145-4556-a4cd-6a27fda4d910
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: FWPM_CONNECTION_CALLBACK0, FWPM_CONNECTION_CALLBACK0 function pointer [Filtering], fwp.fwpm_connection_callback0, fwpmu/FWPM_CONNECTION_CALLBACK0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Fwpmu.h
api_name:
-	FWPM_CONNECTION_CALLBACK0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_CONNECTION_CALLBACK0 callback


## -description


The <b>FWPM_CONNECTION_CALLBACK0</b> function is used to add custom behavior to the connection object subscription process.


## -parameters




### -param *context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://msdn.microsoft.com/86fe40b0-aada-44e1-91dd-0e825589159d">FwpmConnectionSubscribe0</a> function.


### -param eventType [in]

Type: <b><a href="https://msdn.microsoft.com/654b0b66-17b3-4108-af10-1047d07ab2ee">FWPM_CONNECTION_EVENT_TYPE</a></b>

The type of connection object change event.


### -param *connection [in]

Type: <b>const <a href="https://msdn.microsoft.com/76a923d4-57a9-47ba-af91-ee33c3c5b34b">FWPM_CONNECTION0</a>*</b>

The connection object change information.


## -returns



This function pointer does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/86fe40b0-aada-44e1-91dd-0e825589159d">FwpmConnectionSubscribe0</a> to register this callback function.




## -see-also




<a href="https://msdn.microsoft.com/76a923d4-57a9-47ba-af91-ee33c3c5b34b">FWPM_CONNECTION0</a>



<a href="https://msdn.microsoft.com/654b0b66-17b3-4108-af10-1047d07ab2ee">FWPM_CONNECTION_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/86fe40b0-aada-44e1-91dd-0e825589159d">FwpmConnectionSubscribe0</a>
 

 

