---
UID: NF:d2d1.ID2D1Geometry.ComputeLength(const D2D1_MATRIX_3X2_F &,FLOAT,FLOAT)
title: ID2D1Geometry::ComputeLength(const D2D1_MATRIX_3X2_F &,FLOAT,FLOAT)
author: windows-sdk-content
description: Calculates the length of the geometry as though each segment were unrolled into a line.
old-location: direct2d\ID2D1Geometry_ComputeLength_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_FLOAT.htm
tech.root: direct2d
ms.assetid: 8f91ceca-c862-4173-b819-2a2668845c29
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ComputeLength, ComputeLength method [Direct2D], ComputeLength method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],ComputeLength method, ID2D1Geometry.ComputeLength, ID2D1Geometry.ComputeLength(const D2D1_MATRIX_3X2_F &,FLOAT,FLOAT), ID2D1Geometry::ComputeLength, ID2D1Geometry::ComputeLength(const D2D1_MATRIX_3X2_F &,FLOAT,FLOAT), d2d1/ID2D1Geometry::ComputeLength, direct2d.ID2D1Geometry_ComputeLength_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_FLOAT
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1Geometry.ComputeLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Geometry::ComputeLength(const D2D1_MATRIX_3X2_F &,FLOAT,FLOAT)


## -description


Calculates the length of the geometry as though each segment were unrolled into a line. 


## -parameters




### -param worldTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the geometry before calculating its length, or <b>NULL</b>.


#### - flatteningTolerance

Type: <b>FLOAT</b>

The maximum error allowed when constructing a polygonal approximation of the geometry. No point in the polygonal representation will diverge from the original geometry by more than the flattening tolerance. Smaller values produce more accurate results but cause slower execution. 



### -param length [out]

Type: <b>FLOAT*</b>

When this method returns, contains a pointer to the length of the geometry. For closed geometries, the length includes an implicit closing segment. You must allocate storage for this parameter.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

