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

# PackDDElParam function


## -description


Packs a Dynamic Data Exchange (DDE) <i>lParam</i> value into an internal structure used for sharing DDE data between processes.


## -parameters




### -param msg [in]

Type: <b>UINT</b>

The DDE message to be posted.


### -param uiLo [in]

Type: <b>UINT_PTR</b>

A value that corresponds to the 16-bit Windows low-order word of an <i>lParam</i> parameter for the DDE message being posted.


### -param uiHi [in]

Type: <b>UINT_PTR</b>

A value that corresponds to the 16-bit Windows high-order word of an <i>lParam</i> parameter for the DDE message being posted.


## -returns



Type: <b>LPARAM</b>

The return value is the <i>lParam</i> value.




## -remarks



The return value must be posted as the <i>lParam</i> parameter of a DDE message; it must not be used for any other purpose. After the application posts a return value, it need not perform any action to dispose of the <i>lParam</i> parameter.

An application should call this function only for posted DDE messages.




## -see-also




<a href="https://msdn.microsoft.com/0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/166cd1ed-2885-4275-8d92-76ae5344dd92">FreeDDElParam</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/069ac8ee-3d92-4969-8c6b-78a8a0c76721">ReuseDDElParam</a>



<a href="https://msdn.microsoft.com/a7da276f-0e29-4abc-86cf-ac1fd23d84b0">UnpackDDElParam</a>
 

 

