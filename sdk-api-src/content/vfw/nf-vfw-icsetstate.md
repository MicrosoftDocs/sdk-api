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

# ICSetState macro


## -description



The <b>ICSetState</b> macro notifies a video compression driver to set the state of the compressor. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/d1a91847-2893-4c8b-9ca1-02db71ec2c81">ICM_SETSTATE</a> message.




## -parameters




### -param hic

Handle of the compressor. 


### -param pv

Pointer to a block of memory containing configuration data. You can specify <b>NULL</b> for this parameter to reset the compressor to its default state. 


### -param cb

Size, in bytes, of the block of memory. 


## -remarks



The information used by this message is private and specific to a given compressor. Client applications should use this message only to restore information previously obtained with the <a href="https://msdn.microsoft.com/e0066cc2-a67d-4cf4-9d22-506cc152ec14">ICGetState</a> and <a href="https://msdn.microsoft.com/58dbe8ff-4236-456c-8361-e7716e764f89">ICConfigure</a> macros and should use the <b>ICConfigure</b> macro to adjust the configuration of a video compression driver.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

