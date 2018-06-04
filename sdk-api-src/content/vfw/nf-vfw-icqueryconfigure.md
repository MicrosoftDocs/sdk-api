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

# ICQueryConfigure macro


## -description



The <b>ICQueryConfigure</b> macro queries a video compression driver to determine if it has a configuration dialog box. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/9760788e-fa66-44d7-bda6-aa9536143774">ICM_CONFIGURE</a> message.




## -parameters




### -param hic

Handle of the compressor. 


## -remarks



This message is different from the <a href="https://msdn.microsoft.com/0d99fad7-ce79-4574-9fd8-262f7e758866">DRV_CONFIGURE</a> message used for hardware configuration. The dialog box for this message should let the user set and edit the internal state referenced by the <a href="https://msdn.microsoft.com/4b77e294-f3aa-45f9-a4f4-f103b83eae8d">ICM_GETSTATE</a> and <a href="https://msdn.microsoft.com/d1a91847-2893-4c8b-9ca1-02db71ec2c81">ICM_SETSTATE</a> messages. For example, this dialog box can let the user change parameters affecting the quality level and other similar compression options.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

