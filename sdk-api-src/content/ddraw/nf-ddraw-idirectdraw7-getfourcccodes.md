---
UID: NF:ddraw.IDirectDraw7.GetFourCCCodes
title: IDirectDraw7::GetFourCCCodes
author: windows-sdk-content
description: Retrieves the four-character codes (FOURCC) that are supported by the DirectDraw object. This method can also retrieve the number of codes that are supported.
old-location: directdraw\idirectdraw7_getfourcccodes.htm
old-project: directdraw
ms.assetid: 980b1cfe-d466-42f4-865f-6ddc7a41ea94
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFourCCCodes, GetFourCCCodes method [DirectDraw], GetFourCCCodes method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetFourCCCodes method, IDirectDraw7.GetFourCCCodes, IDirectDraw7::GetFourCCCodes, ddraw/IDirectDraw7::GetFourCCCodes, directdraw.idirectdraw7_getfourcccodes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.GetFourCCCodes
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7::GetFourCCCodes


## -description


Retrieves the four-character codes (FOURCC) that are supported by the DirectDraw object. This method can also retrieve the number of codes that are supported.



## -parameters




### -param






#### - lpNumCodes [in, out]

A pointer to a variable that contains the number of entries that the array specified by <i>lpCodes</i> can hold. If the number of entries is too small to accommodate all the codes, <i>lpNumCodes</i> is set to the required number, and the array specified by <i>lpCodes</i> is filled with all that fits.


#### - lpCodes [in, out]

An array of variables to be filled with FOURCCs that are supported by this DirectDraw object. If you specify NULL, <i>lpNumCodes</i> is set to the number of supported FOURCCs, and the method returns.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetFourCCCodes</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

