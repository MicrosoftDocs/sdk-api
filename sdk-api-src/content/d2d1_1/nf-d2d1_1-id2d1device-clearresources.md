---
UID: NF:d2d1_1.ID2D1Device.ClearResources
title: ID2D1Device::ClearResources
author: windows-sdk-content
description: Clears all of the rendering resources used by Direct2D.
old-location: direct2d\id2d1device_clearresources.htm
tech.root: direct2d
ms.assetid: 310817b7-0548-4846-9d36-98842c06a450
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ClearResources, ClearResources method [Direct2D], ClearResources method [Direct2D],ID2D1Device interface, ID2D1Device interface [Direct2D],ClearResources method, ID2D1Device.ClearResources, ID2D1Device::ClearResources, d2d1_1/ID2D1Device::ClearResources, direct2d.id2d1device_clearresources
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
req.lib: D2d1.lib
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
 - ID2D1Device.ClearResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device::ClearResources


## -description


Clears all of the rendering resources used by Direct2D. 


## -parameters




### -param millisecondsSinceUse

Type: <b>UINT</b>

Discards only resources that haven't been used for greater than the specified time in milliseconds. The default is 0 milliseconds.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>
 

 

