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

# GetDCBrushColor function


## -description


The <b>GetDCBrushColor</b> function retrieves the current brush color for the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the DC whose brush color is to be returned.


## -returns



If the function succeeds, the return value is the <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value for the current DC brush color.

If the function fails, the return value is CLR_INVALID.




## -remarks



For information on setting the brush color, see <a href="https://msdn.microsoft.com/4feed536-2f1d-4a25-8311-7cae303167ca">SetDCBrushColor</a>.

<b>ICM:</b> Color management is performed if ICM is enabled.




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/4feed536-2f1d-4a25-8311-7cae303167ca">SetDCBrushColor</a>
 

 

