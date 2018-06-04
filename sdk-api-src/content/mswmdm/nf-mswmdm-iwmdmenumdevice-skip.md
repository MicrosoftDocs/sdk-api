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

# IWMDMEnumDevice::Skip


## -description



The <b>Skip</b> method skips over a specified number of devices in the enumeration sequence.




## -parameters




### -param celt [in]

Number of devices to skip.


### -param pceltFetched [out]

Number of devices actually skipped.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



If the requested number of devices to skip is greater than the remaining devices, the return value from <b>Skip</b> is S_FALSE. At this point, <i>pceltFetched</i> must be used to determine the number of interfaces skipped. If you skip to the end of the device array, a subsequent call to <i>Next</i> also returns S_FALSE. For more information about the standard enumerator Skip method, see the Microsoft COM documentation, available at the <a href="http://go.microsoft.com/fwlink/p/?linkid=3282">Microsoft Web site</a>.




## -see-also




<a href="https://msdn.microsoft.com/fcb93d2a-2107-4aa9-9b3a-130044d7dc96">IWMDMEnumDevice Interface</a>
 

 

