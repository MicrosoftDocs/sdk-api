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

# IFhScopeIterator::MoveToNextItem


## -description


Moves to the next item in the inclusion or exclusion list.


## -parameters






## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



If the current item is the last item in the list, or if the list is empty, this method returns <code>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</code>.




## -see-also




<a href="https://msdn.microsoft.com/E8F993BD-CB53-474A-926D-AED0F5A17073">IFhScopeIterator</a>



<a href="https://msdn.microsoft.com/EB732725-497C-4D58-A05C-373732054BE5">IFhScopeIterator::GetItem</a>
 

 

