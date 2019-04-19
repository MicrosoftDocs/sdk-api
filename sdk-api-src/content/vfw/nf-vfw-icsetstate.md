---
UID: NF:vfw.ICSetState
title: ICSetState macro (vfw.h)
author: windows-sdk-content
description: The ICSetState macro notifies a video compression driver to set the state of the compressor. You can use this macro or explicitly call the ICM_SETSTATE message.
old-location: multimedia\icsetstate.htm
tech.root: Multimedia
ms.assetid: 96958fbf-8539-49bc-a2ff-160b7ea8d2ab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICSetState, ICSetState macro [Windows Multimedia], _win32_ICSetState, multimedia.icsetstate, vfw/ICSetState
ms.topic: macro
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICSetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
 

 

