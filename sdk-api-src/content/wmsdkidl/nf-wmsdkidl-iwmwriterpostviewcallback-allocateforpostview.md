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

# IWMWriterPostViewCallback::AllocateForPostView


## -description



The <b>AllocateForPostView</b> method allocates a buffer for use in postviewing operations. The application implements this method.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param cbBuffer [in]

Size of <i>ppBuffer</i>, in bytes.


### -param ppBuffer [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface.


### -param pvContext [in]

Generic pointer, for use by the application.


## -returns



This method is implemented by the application. It should return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/987dd3b4-2245-4640-820c-5a9660ab5e37">IWMWriterPostViewCallback Interface</a>
 

 

