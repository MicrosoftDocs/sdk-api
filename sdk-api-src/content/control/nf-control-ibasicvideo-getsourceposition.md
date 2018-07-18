---
UID: NF:control.IBasicVideo.GetSourcePosition
title: IBasicVideo::GetSourcePosition
author: windows-sdk-content
description: The GetSourcePosition method retrieves the position of the source rectangle.
old-location: dshow\ibasicvideo_getsourceposition.htm
old-project: DirectShow
ms.assetid: 4624e38c-63ff-4860-a899-c70e44e0f8aa
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetSourcePosition, GetSourcePosition method [DirectShow], GetSourcePosition method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetSourcePosition method, IBasicVideo.GetSourcePosition, IBasicVideo::GetSourcePosition, IBasicVideoGetSourcePosition, control/IBasicVideo::GetSourcePosition, dshow.ibasicvideo_getsourceposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
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
tech.root: 
req.typenames: WMPContextMenuInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBasicVideo.GetSourcePosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBasicVideo::GetSourcePosition


## -description



The <code>GetSourcePosition</code> method retrieves the position of the source rectangle.




## -parameters




### -param pLeft [out]

Pointer to a variable that receives the x-coordinate, in pixels.


### -param pTop [out]

Pointer to a variable that receives the y-coordinate, in pixels.


### -param pWidth [out]

Pointer to a variable that receives the width, in pixels.


### -param pHeight [out]

Pointer to a variable that receives the height, in pixels.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method has the same effect as individually calling the <a href="https://msdn.microsoft.com/1ea64dae-d643-44c1-9026-f9b0dcd25ef1">IBasicVideo::get_SourceLeft</a>, <a href="https://msdn.microsoft.com/87ad3699-5a1b-4fa0-b7bd-5ec87758e9fa">IBasicVideo::get_SourceTop</a>, <a href="https://msdn.microsoft.com/6c6f7e01-5f93-4277-b664-c5be0ea42004">IBasicVideo::get_SourceWidth</a>, and <a href="https://msdn.microsoft.com/3f4e779a-cfa9-496d-a021-d24ae3daa5b3">IBasicVideo::get_SourceHeight</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/14f45bdc-2271-459d-b165-c860c8fc3e0b">IBasicVideo Interface</a>
 

 

