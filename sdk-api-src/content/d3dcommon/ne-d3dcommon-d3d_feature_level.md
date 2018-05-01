---
UID: NE:d3dcommon.D3D_FEATURE_LEVEL
title: D3D_FEATURE_LEVEL
author: windows-driver-content
description: Describes the set of features targeted by a Direct3D device.
old-location: direct3d11\d3d_feature_level.htm
old-project: direct3d11
ms.assetid: afbc1a02-1730-4502-af15-b668412d664c
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: 8da2f171-7790-4f89-b422-ce3f6be0762e, D3D_FEATURE_LEVEL, D3D_FEATURE_LEVEL enumeration [Direct3D 11], D3D_FEATURE_LEVEL_10_0, D3D_FEATURE_LEVEL_10_1, D3D_FEATURE_LEVEL_11_0, D3D_FEATURE_LEVEL_11_1, D3D_FEATURE_LEVEL_12_0, D3D_FEATURE_LEVEL_12_1, D3D_FEATURE_LEVEL_9_1, D3D_FEATURE_LEVEL_9_2, D3D_FEATURE_LEVEL_9_3, d3dcommon/D3D_FEATURE_LEVEL, d3dcommon/D3D_FEATURE_LEVEL_10_0, d3dcommon/D3D_FEATURE_LEVEL_10_1, d3dcommon/D3D_FEATURE_LEVEL_11_0, d3dcommon/D3D_FEATURE_LEVEL_11_1, d3dcommon/D3D_FEATURE_LEVEL_12_0, d3dcommon/D3D_FEATURE_LEVEL_12_1, d3dcommon/D3D_FEATURE_LEVEL_9_1, d3dcommon/D3D_FEATURE_LEVEL_9_2, d3dcommon/D3D_FEATURE_LEVEL_9_3, direct3d11.d3d_feature_level
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dcommon.h
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
req.typenames: D3D_FEATURE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3DCommon.h
api_name:
-	D3D_FEATURE_LEVEL
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# D3D_FEATURE_LEVEL enumeration


## -description



      Describes the set of features targeted by a Direct3D device.


## -enum-fields




### -field D3D_FEATURE_LEVEL_9_1


            Targets features supported by <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> 9.1 including shader model 2.
          


### -field D3D_FEATURE_LEVEL_9_2


            Targets features supported by <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> 9.2 including shader model 2.
          


### -field D3D_FEATURE_LEVEL_9_3


            Targets features supported by <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> 9.3 including shader model 2.0b.
          


### -field D3D_FEATURE_LEVEL_10_0


            Targets features supported by Direct3D 10.0 including shader model 4.
          


### -field D3D_FEATURE_LEVEL_10_1


            Targets features supported by Direct3D 10.1 including shader model 4.
          


### -field D3D_FEATURE_LEVEL_11_0


            Targets features supported by Direct3D 11.0 including shader model 5.
          


### -field D3D_FEATURE_LEVEL_11_1


            Targets features supported by Direct3D 11.1 including shader model 5 and logical blend operations. This feature level requires a display driver that is at least implemented to WDDM for Windows 8 (WDDM 1.2).
          


### -field D3D_FEATURE_LEVEL_12_0


            Targets features supported by Direct3D 12.0 including shader model 5.
          


### -field D3D_FEATURE_LEVEL_12_1


            Targets features supported by Direct3D 12.1 including shader model 5.
          


## -remarks




          For an overview of
          the capabilities of each feature level, see <a href="overviews_direct3d_11_devices_downlevel_intro.htm">Overview For Each Feature Level</a>.
        


          For information about limitations creating non-hardware-type devices on certain feature levels, see <a href="https://msdn.microsoft.com/7e022e5d-daa3-48fa-b9fe-4b569220e55e">Limitations Creating WARP and Reference Devices</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

