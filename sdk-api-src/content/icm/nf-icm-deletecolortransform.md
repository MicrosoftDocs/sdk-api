---
UID: NF:icm.DeleteColorTransform
title: DeleteColorTransform function
author: windows-sdk-content
description: The DeleteColorTransform function deletes a given color transform.
old-location: wcs\deletecolortransform.htm
tech.root: WCS
ms.assetid: 2efd98d8-851f-4a6c-b91b-2430895a7a53
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DeleteColorTransform, DeleteColorTransform function [Windows Color System], _color_DeleteColorTransform, icm/DeleteColorTransform, wcs.deletecolortransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
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
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - DeleteColorTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DeleteColorTransform
: 
---

# DeleteColorTransform function


## -description


The <b>DeleteColorTransform</b> function deletes a given color transform.


## -parameters




### -param hxform

Identifies the color transform to delete.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/bf344e44-1379-4ba5-8215-57001c53bbd5">CreateMultiProfileTransform</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="color.htm">The COLOR Structure</a>
 

 

