---
UID: NF:control.IBasicVideo.GetDestinationPosition
title: IBasicVideo::GetDestinationPosition
author: windows-sdk-content
description: The GetDestinationPosition method retrieves the position of the destination rectangle.
old-location: dshow\ibasicvideo_getdestinationposition.htm
old-project: DirectShow
ms.assetid: ee2abf52-edc2-471e-bf9b-eda04f2eabe4
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetDestinationPosition, GetDestinationPosition method [DirectShow], GetDestinationPosition method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetDestinationPosition method, IBasicVideo.GetDestinationPosition, IBasicVideo::GetDestinationPosition, IBasicVideoGetDestinationPosition, control/IBasicVideo::GetDestinationPosition, dshow.ibasicvideo_getdestinationposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.redist: 
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
 - IBasicVideo.GetDestinationPosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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



This method has the same effect as individually calling the <a href="https://msdn.microsoft.com/578f5bbd-23b0-4100-a1d8-0987381fd56f">IBasicVideo::get_DestinationLeft</a>, <a href="https://msdn.microsoft.com/79690655-ac84-4119-9d87-799990424f00">IBasicVideo::get_DestinationTop</a>, <a href="https://msdn.microsoft.com/6e27bb57-ca88-4478-86b8-250a69f5fc78">IBasicVideo::get_DestinationWidth</a>, and <a href="https://msdn.microsoft.com/21d6c74a-2adb-4015-b0df-5acb26c22212">IBasicVideo::get_DestinationHeight</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/14f45bdc-2271-459d-b165-c860c8fc3e0b">IBasicVideo Interface</a>
 

 

