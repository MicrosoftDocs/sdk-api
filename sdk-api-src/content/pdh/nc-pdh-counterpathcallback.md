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

# CounterPathCallBack callback function


## -description



			Applications implement the <b>CounterPathCallBack</b> function to process the counter path strings returned by the  <b>Browse</b> dialog box.
		


## -parameters




### -param Arg1








#### - dwArg [in]

User-defined value passed to the callback function by the <b>Browse</b> dialog box. You set this value in the <b>dwCallBackArg</b> member of the 
<a href="https://msdn.microsoft.com/8e045e0b-c157-4527-902c-6096c7922642">PDH_BROWSE_DLG_CONFIG</a> structure.


## -returns



Return ERROR_SUCCESS if the function succeeds. 

If the function fails due to a transient error, you can return PDH_RETRY and PDH will call your callback immediately.

Otherwise, return an appropriate error code. The error code is passed back to the caller of <a href="https://msdn.microsoft.com/4e9e4b20-a573-4f6d-97e8-63bcc675032b">PdhBrowseCounters</a>.




## -remarks



The following members of the 
<a href="https://msdn.microsoft.com/8e045e0b-c157-4527-902c-6096c7922642">PDH_BROWSE_DLG_CONFIG</a> structure are used to communicate with the callback function:






## -see-also




<a href="https://msdn.microsoft.com/8e045e0b-c157-4527-902c-6096c7922642">PDH_BROWSE_DLG_CONFIG</a>



<a href="https://msdn.microsoft.com/4e9e4b20-a573-4f6d-97e8-63bcc675032b">PdhBrowseCounters</a>
 

 

