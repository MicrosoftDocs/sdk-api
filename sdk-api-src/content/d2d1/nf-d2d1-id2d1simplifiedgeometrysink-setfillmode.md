---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.SetFillMode
title: ID2D1SimplifiedGeometrySink::SetFillMode (d2d1.h)
author: windows-sdk-content
description: Specifies the method used to determine which points are inside the geometry described by this geometry sink and which points are outside.
old-location: direct2d\ID2D1SimplifiedGeometrySink_SetFillMode.htm
tech.root: Direct2D
ms.assetid: f60f48bb-989e-46a5-b77f-65da0b91a599
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1SimplifiedGeometrySink interface [Direct2D],SetFillMode method, ID2D1SimplifiedGeometrySink.SetFillMode, ID2D1SimplifiedGeometrySink::SetFillMode, SetFillMode, SetFillMode method [Direct2D], SetFillMode method [Direct2D],ID2D1SimplifiedGeometrySink interface, d2d1/ID2D1SimplifiedGeometrySink::SetFillMode, direct2d.ID2D1SimplifiedGeometrySink_SetFillMode
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - ID2D1SimplifiedGeometrySink.SetFillMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SimplifiedGeometrySink::SetFillMode


## -description


Specifies the method used to determine which points are inside the geometry described by this geometry sink  and which points are outside. 


## -parameters




### -param fillMode

Type: <b><a href="https://msdn.microsoft.com/f1a14447-39fa-4a48-9516-ff5b03abc3a6">D2D1_FILL_MODE</a></b>

The method used to determine whether a given point is part of the geometry.


## -returns



This method does not return a value.




## -remarks



The fill mode defaults to D2D1_FILL_MODE_ALTERNATE. To set the fill mode, call <b>SetFillMode</b> before the first call to <a href="https://msdn.microsoft.com/87a932d4-1f90-4bdb-b131-0664566b0318">BeginFigure</a>. Not doing will put the geometry sink in an error state. 




## -see-also




<a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>
 

 

