---
UID: NF:control.IBasicVideo.GetDestinationPosition
title: IBasicVideo::GetDestinationPosition
author: windows-sdk-content
description: The GetDestinationPosition method retrieves the position of the destination rectangle.
old-location: dshow\ibasicvideo_getdestinationposition.htm
tech.root: DirectShow
ms.assetid: ee2abf52-edc2-471e-bf9b-eda04f2eabe4
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetDestinationPosition, GetDestinationPosition method [DirectShow], GetDestinationPosition method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetDestinationPosition method, IBasicVideo.GetDestinationPosition, IBasicVideo::GetDestinationPosition, IBasicVideoGetDestinationPosition, control/IBasicVideo::GetDestinationPosition, dshow.ibasicvideo_getdestinationposition
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBasicVideo.GetDestinationPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBasicVideo::GetDestinationPosition


## -description



The <code>GetDestinationPosition</code> method retrieves the position of the destination rectangle.




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



This method has the same effect as individually calling the <a href="https://msdn.microsoft.com/en-us/library/Dd389579(v=VS.85).aspx">IBasicVideo::get_DestinationLeft</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd389580(v=VS.85).aspx">IBasicVideo::get_DestinationTop</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd389581(v=VS.85).aspx">IBasicVideo::get_DestinationWidth</a>, and <a href="https://msdn.microsoft.com/en-us/library/Dd389578(v=VS.85).aspx">IBasicVideo::get_DestinationHeight</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd389540(v=VS.85).aspx">IBasicVideo Interface</a>
 

 

