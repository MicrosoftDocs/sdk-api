---
UID: NF:mfapi.Pack2UINT32AsUINT64
title: Pack2UINT32AsUINT64 function (mfapi.h)
author: windows-sdk-content
description: Packs two UINT32 values into a UINT64 value.
old-location: mf\pack2uint32asuint64.htm
tech.root: medfound
ms.assetid: 82d37211-e2e5-4b34-8102-2c3f8650cc26
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Pack2UINT32AsUINT64, Pack2UINT32AsUINT64 function [Media Foundation], mf.pack2uint32asuint64, mfapi/Pack2UINT32AsUINT64
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - Pack2UINT32AsUINT64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Pack2UINT32AsUINT64 function


## -description


Packs two <b>UINT32</b> values into a <b>UINT64</b> value.


## -parameters




### -param unHigh [in]

Value to store in the high-order 32 bits of the <b>UINT64</b> value.


### -param unLow [in]

Value to store in the low-order 32 bits of the <b>UINT64</b> value.


## -returns



Returns the packed <b>UINT64</b> value.




## -remarks



This function stores two 32-bit values in a 64-bit value that is suitable for the <a href="https://msdn.microsoft.com/817ed1c1-16ad-4520-a1a0-a93563936b50">IMFAttributes::SetUINT64</a> method.




## -see-also




<a href="https://msdn.microsoft.com/04e8c89e-115e-41d4-b8cb-953f68ddd14e">MFSetAttributeRatio</a>



<a href="https://msdn.microsoft.com/cf7b3cfe-fdce-417d-8c0b-198d026b8768">MFSetAttributeSize</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

