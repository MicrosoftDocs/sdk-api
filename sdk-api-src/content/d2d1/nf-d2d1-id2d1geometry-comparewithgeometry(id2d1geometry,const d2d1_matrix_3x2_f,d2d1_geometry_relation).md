---
UID: NF:d2d1.ID2D1Geometry.CompareWithGeometry(ID2D1Geometry,const D2D1_MATRIX_3X2_F,D2D1_GEOMETRY_RELATION)
title: ID2D1Geometry::CompareWithGeometry(ID2D1Geometry,const D2D1_MATRIX_3X2_F,D2D1_GEOMETRY_RELATION)
author: windows-sdk-content
description: Describes the intersection between this geometry and the specified geometry. The comparison is performed using the default flattening tolerance.
old-location: direct2d\ID2D1Geometry_CompareWithGeometry_ptr_ID2D1Geometry_ptr_D2D_MATRIX_3X2_F_ptr_D2D1_GEOMETRY_RELATION.htm
tech.root: direct2d
ms.assetid: 49887b1a-24ca-4c1c-8c70-b53a995028fd
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: CompareWithGeometry, CompareWithGeometry method [Direct2D], CompareWithGeometry method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],CompareWithGeometry method, ID2D1Geometry.CompareWithGeometry, ID2D1Geometry.CompareWithGeometry(ID2D1Geometry,const D2D1_MATRIX_3X2_F,D2D1_GEOMETRY_RELATION), ID2D1Geometry::CompareWithGeometry, ID2D1Geometry::CompareWithGeometry(ID2D1Geometry,const D2D1_MATRIX_3X2_F,D2D1_GEOMETRY_RELATION), d2d1/ID2D1Geometry::CompareWithGeometry, direct2d.ID2D1Geometry_CompareWithGeometry_ptr_ID2D1Geometry_ptr_D2D_MATRIX_3X2_F_ptr_D2D1_GEOMETRY_RELATION
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
 - ID2D1Geometry.CompareWithGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Geometry::CompareWithGeometry(ID2D1Geometry,const D2D1_MATRIX_3X2_F,D2D1_GEOMETRY_RELATION)


## -description


Describes the intersection between this geometry and the specified geometry. The comparison is performed using the default flattening tolerance.


## -parameters




### -param inputGeometry [in]

Type: <b><a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>*</b>

The geometry to test.


### -param inputGeometryTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to <i>inputGeometry</i>, or <b>NULL</b>.


### -param relation [out]

Type: <b><a href="https://msdn.microsoft.com/6c7290c8-9363-414b-af2c-0f2a79da99f9">D2D1_GEOMETRY_RELATION</a>*</b>

When this method returns, contains a pointer to a value that describes how this geometry is related to <i>inputGeometry</i>. You must allocate storage for this parameter.  


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When interpreting the returned <i>relation</i> value, it is important to remember that the member <a href="https://msdn.microsoft.com/6c7290c8-9363-414b-af2c-0f2a79da99f9">D2D1_GEOMETRY_RELATION_IS_CONTAINED</a> of the  <b>D2D1_GEOMETRY_RELATION</b> enumeration type means that this geometry is contained  inside <i>inputGeometry</i>, not that this geometry contains <i>inputGeometry</i>. 

For  more information about how to interpret other possible return values, see <a href="https://msdn.microsoft.com/6c7290c8-9363-414b-af2c-0f2a79da99f9">D2D1_GEOMETRY_RELATION</a>.




## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

