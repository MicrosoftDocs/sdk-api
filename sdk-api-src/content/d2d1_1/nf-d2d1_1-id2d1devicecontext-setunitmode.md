---
UID: NF:d2d1_1.ID2D1DeviceContext.SetUnitMode
title: ID2D1DeviceContext::SetUnitMode
author: windows-sdk-content
description: Sets what units will be used to interpret values passed into the device context.
old-location: direct2d\id2d1devicecontext_setunitmode.htm
tech.root: Direct2D
ms.assetid: a5774b9a-4458-47e7-821a-4ac4b70468e3
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],SetUnitMode method, ID2D1DeviceContext.SetUnitMode, ID2D1DeviceContext::SetUnitMode, SetUnitMode, SetUnitMode method [Direct2D], SetUnitMode method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::SetUnitMode, direct2d.id2d1devicecontext_setunitmode
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
 - ID2D1DeviceContext.SetUnitMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::SetUnitMode


## -description


Sets what units will be used to interpret values passed into the device context.




## -parameters




### -param unitMode

Type: <b><a href="https://msdn.microsoft.com/1ba11761-f3e9-4996-8494-384db5bddc99">D2D1_UNIT_MODE</a></b>

An enumeration defining how passed-in units will be interpreted by the device context.


## -returns



This method does not return a value.




## -remarks



This method will affect all properties and parameters affected by <a href="https://msdn.microsoft.com/603a838b-4abc-4adf-93a9-ec8535d42ed6">SetDpi</a> 
        and <a href="https://msdn.microsoft.com/72a25b78-96fd-42bf-9e71-6bb80efea0ac">GetDpi</a>. This affects all coordinates, lengths, and other properties that are 
        not explicitly defined as being in another unit. For example:

<ul>
<li><b>SetUnitMode</b> will affect a coordinate passed 
            into <a href="https://msdn.microsoft.com/7eb70308-4142-4d32-a070-9e937579b896">ID2D1DeviceContext::DrawLine</a>, and the scaling of a 
            geometry passed into <a href="https://msdn.microsoft.com/097f21ac-a062-4ce1-bdc7-87317dbdf5be">ID2D1DeviceContext::FillGeometry</a>.
          </li>
<li><b>SetUnitMode</b> will not affect the value
            returned by <a href="https://msdn.microsoft.com/0d51408a-2648-4984-bbc0-9846d5161c77">ID2D1Bitmap::GetPixelSize</a>.
          </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/1ba11761-f3e9-4996-8494-384db5bddc99">D2D1_UNIT_MODE</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

