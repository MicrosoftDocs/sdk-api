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

# IEnumWbemClassObject::Reset


## -description


The 
<b>IEnumWbemClassObject::Reset</b> method resets an enumeration sequence back to the beginning. Because CIM objects are dynamic, calling this method does not necessarily return the same list of objects that you obtained previously.
<div class="alert"><b>Note</b>  This method fails if the enumerator was originally created with the <b>WBEM_FLAG_FORWARD_ONLY</b> option.</div><div> </div>

## -parameters






## -returns



The 
<b>Reset</b> method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



The COM-specific error codes may also be returned if the remote connection to the Windows Management is lost due to network problems.

You may see COM-specific error codes returned if network problems cause you to lose the remote connection to Windows Management.

If <b>WBEM_S_NO_ERROR</b> is not returned, you can call the COM function <b>GetErrorInfo</b> to get  more information about the error.



