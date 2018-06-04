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

# IAsyncReader::EndFlush


## -description



The <code>EndFlush</code> method ends a flush operation.




## -parameters






## -returns



Returns S_OK if successful, or S_FALSE otherwise.




## -remarks



While the pin is flushing, the <a href="https://msdn.microsoft.com/d0eab370-bb17-48fa-9926-6a6eeaba5603">IAsyncReader::Request</a> method fails and the <a href="https://msdn.microsoft.com/fc54f917-3b86-4c0b-b356-217bc9793504">IAsyncReader::WaitForNext</a> method returns immediately. Call the <code>EndFlush</code> method at the end of a flush operation, to reenable the <b>Request</b> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54a18567-e9d4-4b12-b486-cdd70d719184">IAsyncReader Interface</a>
 

 

