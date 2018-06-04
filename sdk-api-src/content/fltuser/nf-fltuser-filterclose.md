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

# FilterClose function


## -description


The <b>FilterClose</b> function closes an open minifilter handle. 


## -parameters




### -param hFilter [in]

Minifilter handle returned by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540467">FilterCreate</a>. 


## -returns



<b>FilterClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After <b>FilterClose</b> is called, the minifilter handle that the <i>hFilter</i> parameter specifies is no longer valid and cannot safely be used. 

Use <b>FilterClose</b> to close open minifilter handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540467">FilterCreate</a>. Use <a href="https://msdn.microsoft.com/library/windows/hardware/ff540481">FilterFindClose</a> to close handles returned by calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540485">FilterFindFirst</a>. 

To close a connection port handle that was opened by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff540460">FilterConnectCommunicationPort</a>, use <a href="http://go.microsoft.com/fwlink/p/?linkid=139078">CloseHandle</a>. 




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=139078">CloseHandle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540460">FilterConnectCommunicationPort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540467">FilterCreate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540481">FilterFindClose</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540485">FilterFindFirst</a>
 

 

