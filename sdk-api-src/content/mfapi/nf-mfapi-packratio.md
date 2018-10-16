---
UID: NF:mfapi.PackRatio
title: PackRatio function
author: windows-sdk-content
description: Packs two UINT32 values, which represent a ratio, into a UINT64 value.
old-location: mf\packratio.htm
tech.root: medfound
ms.assetid: 2E175E21-D5A3-43B1-8AB9-A427E0F9350E
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: PackRatio, PackRatio function [Media Foundation], mf.packratio, mfapi/PackRatio
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
 - PackRatio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PackRatio function


## -description


Packs two UINT32 values, which represent a ratio, into a UINT64 value.


## -parameters




### -param nNumerator [in]

Value to store the <b>UINT32</b> numerator value.


### -param unDenominator [in]

Value to store the <b>UINT32</b> denominator value.


## -returns



Returns the packed <b>UINT64</b> value.




## -remarks



This function stores two 32-bit values in a 64-bit value that is suitable for the <a href="https://msdn.microsoft.com/817ed1c1-16ad-4520-a1a0-a93563936b50">IMFAttributes::SetUINT64</a> method.




## -see-also




<a href="https://msdn.microsoft.com/2572c30c-4ae1-42b7-b1f7-6c564d936c60">MFGetAttributeRatio</a>



<a href="https://msdn.microsoft.com/c74445b2-a2ec-4c77-a8bf-61a6b54cef75">MFGetAttributeSize</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

