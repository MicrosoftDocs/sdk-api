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

# ITuningSpace::get_DefaultLocator


## -description



The <b>get_DefaultLocator</b> method retrieves the default locator for this tuning space.




## -parameters




### -param LocatorVal






#### - ppLocatorVal [out]

Address of a variable that receives a pointer to <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a> interface. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The tuning space might not have a default locator. It is the application's responsibility to provide a default locator for the tuning space if needed.

If the tuning space does not have a default locator, this method succeeds but returns the value <b>NULL</b> in the <i>ppLocatorVal</i> parameter. Check for a <b>NULL</b> value before attempting to dereference the pointer.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>



<a href="https://msdn.microsoft.com/59065cc9-8a11-4551-ad3d-e7963628aa20">ITuningSpace::put_DefaultLocator</a>
 

 

