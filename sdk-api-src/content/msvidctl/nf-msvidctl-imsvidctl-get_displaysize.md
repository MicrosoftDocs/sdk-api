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

# IMSVidCtl::get_DisplaySize


## -description


The <b>get_DisplaySize</b> method retrieves the display size.


## -parameters




### -param CurrentValue






#### - pCurrentValue [out]

Receives a member of the <a href="https://msdn.microsoft.com/2e939cbc-fc75-41d7-9fcb-32da5173f9bc">DisplaySizeList</a> enumeration.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The display size has no effect if the <b>AutoSize</b> property is false.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/8adbc701-fd05-4520-8f06-95bd67a08d1e">IMSVidCtl::get_AutoSize</a>



<a href="https://msdn.microsoft.com/1771e66b-e5f3-44f5-a489-e57baaf5cf25">IMSVidCtl::put_DisplaySize</a>
 

 

