---
UID: NF:mfapi.UnpackRatio
title: UnpackRatio function
author: windows-sdk-content
description: Gets the low-order and high-order UINT32 values from a UINT64 value that represents a ratio.
old-location: mf\unpackratio.htm
tech.root: medfound
ms.assetid: 8E4E1E6C-1C80-4A0B-98CE-2ED3443E1821
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: UnpackRatio, mf.unpackratio, mfapi/unpackratio, unpackratio, unpackratio function [Media Foundation]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - unpackratio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnpackRatio function


## -description


Gets the low-order and high-order <b>UINT32</b> values from a <b>UINT64</b> value that represents a ratio.


## -parameters




### -param unPacked [in]

The value to convert.


### -param pnNumerator [out]

Receives the high-order 32 bits.


### -param punDenominator [out]

Receives the low-order 32 bits.


## -returns



This function does not return a value.




## -remarks



You can use this function to unpack a <b>UINT64</b> value that you receive from the <a href="https://msdn.microsoft.com/f3240fff-48d8-4d88-8c75-15f00bfe72ed">IMFAttributes::GetUINT64</a> method.




## -see-also




<a href="https://msdn.microsoft.com/2572c30c-4ae1-42b7-b1f7-6c564d936c60">MFGetAttributeRatio</a>



<a href="https://msdn.microsoft.com/c74445b2-a2ec-4c77-a8bf-61a6b54cef75">MFGetAttributeSize</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

