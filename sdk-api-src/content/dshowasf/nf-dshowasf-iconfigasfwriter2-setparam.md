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

# IConfigAsfWriter2::SetParam


## -description



The <code>SetParam</code> method sets the value of the specified filter configuration parameter.




## -parameters




### -param dwParam [in]

Specifies the parameter to set,as a member of the <a href="https://msdn.microsoft.com/aa274c86-f75d-40ee-8c46-918ccffdfd03">_AM_ASFWRITERCONFIG_PARAM</a> enumeration.


### -param dwParam1 [in]

Specifies the value to assign to the <i>dwParam</i> parameter.


### -param dwParam2 [out]

Reserved. Must be zero.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/fd931a95-3678-46de-8f17-9e7c27087398">IConfigAsfWriter2 Interface</a>
 

 

