---
UID: NF:wingdi.DeleteObject
title: DeleteObject function
author: windows-sdk-content
description: The DeleteObject function deletes a logical pen, brush, font, bitmap, region, or palette, freeing all system resources associated with the object. After the object is deleted, the specified handle is no longer valid.
old-location: gdi\deleteobject.htm
old-project: gdi
ms.assetid: cc679af0-6839-4c83-9c42-39d7ededda40
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DeleteObject, DeleteObject function [Windows GDI], DeleteObjectW, _win32_DeleteObject, gdi.deleteobject, wingdi/DeleteObject, wingdi/DeleteObjectW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteObjectW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-RTCore-GDI-object-l1-1-0.dll
 - api-ms-win-gdi-ie-rgn-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-gdi-dc-l1-1-0.dll
api_name:
 - DeleteObject
 - DeleteObjectW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DeleteObject function


## -description


The <b>DeleteObject</b> function deletes a logical pen, brush, font, bitmap, region, or palette, freeing all system resources associated with the object. After the object is deleted, the specified handle is no longer valid.


## -parameters




### -param ho

TBD




#### - hObject [in]

A handle to a logical pen, brush, font, bitmap, region, or palette.


## -returns



If the function succeeds, the return value is nonzero.

If the specified handle is not valid or is currently selected into a DC, the return value is zero.




## -remarks



Do not delete a drawing object (pen or brush) while it is still selected into a DC.

When a pattern brush is deleted, the bitmap associated with the brush is not deleted. The bitmap must be deleted independently.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/2ea32786-f769-4096-8f60-f924c83ca9c8">Creating Colored Pens and Brushes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

