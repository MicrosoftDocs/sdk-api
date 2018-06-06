---
UID: NF:ddraw.IDirectDraw7.TestCooperativeLevel
title: IDirectDraw7::TestCooperativeLevel
author: windows-sdk-content
description: Reports the current cooperative-level status of the DirectDraw device for a windowed or full-screen application.
old-location: directdraw\idirectdraw7_testcooperativelevel.htm
old-project: directdraw
ms.assetid: 6bbabd8c-f48e-480c-9ea4-06e4fce1255a
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],TestCooperativeLevel method, IDirectDraw7.TestCooperativeLevel, IDirectDraw7::TestCooperativeLevel, TestCooperativeLevel, TestCooperativeLevel method [DirectDraw], TestCooperativeLevel method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::TestCooperativeLevel, directdraw.idirectdraw7_testcooperativelevel
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
 - IDirectDraw7.TestCooperativeLevel
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7::TestCooperativeLevel


## -description


Reports the current cooperative-level status of the DirectDraw device for a windowed or full-screen application.



## -parameters






## -returns



If the method succeeds, the return value is DD_OK, which indicates that the calling application can continue.

If it fails, the method can return one of the following error values (see Remarks):

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_EXCLUSIVEMODEALREADYSET</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_WRONGMODE</li>
</ul>



## -remarks



This method is particularly useful to applications that use the WM_ACTIVATEAPP and WM_DISPLAYCHANGE system messages as a notification to restore surfaces or recreate DirectDraw objects. The DD_OK return value always indicates that the application can continue, but the error codes are interpreted differently, depending on the cooperative level that the application uses.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>TestCooperativeLevel</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

