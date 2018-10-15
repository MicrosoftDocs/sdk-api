---
UID: NF:d2d1_1.ID2D1CommandSink.SetUnitMode
title: ID2D1CommandSink::SetUnitMode
author: windows-sdk-content
description: The unit mode changes the meaning of subsequent units from device-independent pixels (DIPs) to pixels or the other way. The command sink does not record a DPI, this is implied by the playback context or other playback interface such as ID2D1PrintControl.
old-location: direct2d\id2d1commandsink_setunitmode.htm
tech.root: direct2d
ms.assetid: e524aa51-2499-4333-9562-a4893666b666
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetUnitMode method, ID2D1CommandSink.SetUnitMode, ID2D1CommandSink::SetUnitMode, SetUnitMode, SetUnitMode method [Direct2D], SetUnitMode method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetUnitMode, direct2d.id2d1commandsink_setunitmode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1CommandSink.SetUnitMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::SetUnitMode


## -description


The unit mode changes the meaning of subsequent units from device-independent pixels (DIPs) to pixels  or the other way. The command sink does not record a DPI, this is implied by the playback context or other playback interface such as <a href="https://msdn.microsoft.com/0E8D8218-0671-44A2-AD6E-13BB0B4EB66C">ID2D1PrintControl</a>.


## -parameters




### -param unitMode

Type: <b><a href="https://msdn.microsoft.com/1ba11761-f3e9-4996-8494-384db5bddc99">D2D1_UNIT_MODE</a></b>

The enumeration that specifies how units are to be interpreted.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -remarks



The unit mode changes the interpretation of units from DIPs to pixels  or vice versa.




## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/04799366-6458-40ff-a2fb-5d227eab041d">ID2D1RenderTarget::SetTransform</a>
 

 

