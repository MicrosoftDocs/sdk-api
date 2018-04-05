---
UID: NS:d3d9types._D3DAES_CTR_IV
title: "_D3DAES_CTR_IV"
author: windows-driver-content
description: Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.
old-location: mf\d3daes_ctr_iv.htm
old-project: medfound
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAES_CTR_IV, D3DAES_CTR_IV structure [Media Foundation], _D3DAES_CTR_IV, d3d9types/D3DAES_CTR_IV, mf.d3daes_ctr_iv
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
req.include-header: D3d9.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3DAES_CTR_IV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAES_CTR_IV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAES_CTR_IV structure


## -description


Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.


## -struct-fields




### -field IV

The IV, in big-endian format.


### -field Count

The block count, in big-endian format.


## -remarks



The <b>D3DAES_CTR_IV</b> structure and the <a href="https://msdn.microsoft.com/acde4bbb-2a14-4237-b426-a157a9781f40">DXVA2_AES_CTR_IV</a> structure are equivalent.

For details, see <a href="https://msdn.microsoft.com/acde4bbb-2a14-4237-b426-a157a9781f40">DXVA2_AES_CTR_IV</a>.




## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>
 

 

