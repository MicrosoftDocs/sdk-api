---
UID: NS:dxva._DXVA_Qmatrix_HEVC
title: "_DXVA_Qmatrix_HEVC"
author: windows-driver-content
description: Defines a quantization matrix.
old-location: mf\dxva_qmatrix_hevc.htm
old-project: medfound
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPDXVA_Qmatrix_HEVC, DXVA_Qmatrix_HEVC, DXVA_Qmatrix_HEVC structure [Media Foundation], LPDXVA_Qmatrix_HEVC, LPDXVA_Qmatrix_HEVC structure pointer [Media Foundation], _DXVA_Qmatrix_HEVC, dxva/DXVA_Qmatrix_HEVC, dxva/LPDXVA_Qmatrix_HEVC, mf.dxva_qmatrix_hevc"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva.h
api_name:
-	DXVA_Qmatrix_HEVC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA_Qmatrix_HEVC structure


## -description


Defines a quantization matrix.


## -struct-fields




### -field ucScalingLists0

 


### -field ucScalingLists1

 


### -field ucScalingLists2

 


### -field ucScalingLists3

 


### -field ucScalingListDCCoefSizeID2

Contains the DC value of the scaling list for 16x16 size with sizeID equal to 2 and corresponding to scaling_list_dc_coef_minus8[ sizeID − 2 ][ matrixID ] +8 with sizeID equal to 2 and matrixID in the range of 0 to 5, inclusive, in HEVC specification. 


### -field ucScalingListDCCoefSizeID3

Contains the DC value of the scaling list for 32x32 size with sizeID equal to 3, and corresponding to scaling_list_dc_coef_minus8[ sizeID − 2 ][ matrixID ] +8 with sizeID equal to 3 and matrixID in the range of 0 to 1, inclusive, in HEVC specification. 


#### - ucScalingLists0[6][16]

Contains the scaling lists for the 4x4 scaling process, corresponding to ScalingList[ 0 ][ MatrixID ][ i ] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 15, inclusive. 


#### - ucScalingLists1[6][64]

Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList[ 1 ][ MatrixID ][ i ] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.  


#### - ucScalingLists2[6][64]

Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList[ 2 ][ MatrixID ][ i ] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.  


#### - ucScalingLists3[2][64]

Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList[ 3 ][ MatrixID ][ i ] in HEVC specification, where MatrixID is in the range of 0 to 1, inclusive, and i is in the range of 0 to 63, inclusive. 


## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

