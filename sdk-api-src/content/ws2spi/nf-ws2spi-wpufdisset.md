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

# WPUFDIsSet function


## -description



			The 
<b>WPUFDIsSet</b> function checks the membership of the specified socket handle.


## -parameters




### -param s [in]

Descriptor identifying the socket.


### -param fdset

TBD




#### - set [in]

Set to check for the membership of socket <i>s</i>.


## -returns




						If no error occurs, a value of nonzero is returned denoting that socket <i>s</i> is a member of the <i>set</i> parameter. Otherwise, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/a8f2922d-2474-406d-b1c7-631f05ccdd9c">WSPSelect</a>
 

 

