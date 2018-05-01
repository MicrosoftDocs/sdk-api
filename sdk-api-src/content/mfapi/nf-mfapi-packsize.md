---
UID: NF:mfapi.PackSize
title: PackSize function
author: windows-driver-content
description: Packs a UINT32 width value and a UINT32 height value into a UINT64 value that represents a size.
old-location: mf\packsize.htm
old-project: medfound
ms.assetid: F3DCEEA5-2D88-49FC-87DB-DEB0AE48E984
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PackSize, PackSize function [Media Foundation], mf.packsize, mfapi/PackSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfapi.h
api_name:
-	PackSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# PackSize function


## -description


Packs a UINT32 width value and a UINT32 height value into a UINT64 value that represents a size.


## -parameters




### -param unWidth [in]

Value to store the <b>UINT32</b> width value.


### -param unHeight [in]

Value to store the <b>UINT32</b> height value.


## -returns



Returns the packed <b>UINT64</b> value.




## -remarks



This function stores two 32-bit values in a 64-bit value that is suitable for the <a href="https://msdn.microsoft.com/817ed1c1-16ad-4520-a1a0-a93563936b50">IMFAttributes::SetUINT64</a> method.




## -see-also




<a href="https://msdn.microsoft.com/2572c30c-4ae1-42b7-b1f7-6c564d936c60">MFGetAttributeRatio</a>



<a href="https://msdn.microsoft.com/c74445b2-a2ec-4c77-a8bf-61a6b54cef75">MFGetAttributeSize</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

