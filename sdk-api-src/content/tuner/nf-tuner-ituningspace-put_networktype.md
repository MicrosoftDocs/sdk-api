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

# ITuningSpace::put_NetworkType


## -description



The <b>put_NetworkType</b> method specifies the network type of the tuning space as a <b>BSTR</b>.



This method is intended for Automation clients, because it specifies the CLSID as a <b>BSTR</b>. C++ applications can use the <a href="https://msdn.microsoft.com/02e4ec53-e527-4cd2-a424-66c2f3fe4e43">ITuningSpace::put__NetworkType</a> method instead, which takes a GUID value.


## -parameters




### -param NetworkTypeGuid [in]

Contains the string representation of the network type GUID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

