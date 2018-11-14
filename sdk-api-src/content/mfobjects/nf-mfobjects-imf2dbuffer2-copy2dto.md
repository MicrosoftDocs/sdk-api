---
UID: NF:mfobjects.IMF2DBuffer2.Copy2DTo
title: IMF2DBuffer2::Copy2DTo
author: windows-sdk-content
description: Copies the buffer to another 2D buffer object.
old-location: mf\imf2dbuffer2_copy2dto.htm
tech.root: medfound
ms.assetid: 90B0CBA2-2474-4B34-8BB4-6C59C05CDD7E
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Copy2DTo, Copy2DTo method [Media Foundation], Copy2DTo method [Media Foundation],IMF2DBuffer2 interface, IMF2DBuffer2 interface [Media Foundation],Copy2DTo method, IMF2DBuffer2.Copy2DTo, IMF2DBuffer2::Copy2DTo, mf.imf2dbuffer2_copy2dto, mfobjects/IMF2DBuffer2::Copy2DTo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMF2DBuffer2.Copy2DTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfobjects.h
: 
- IMF2DBuffer2.Copy2DTo
: 
---

# IMF2DBuffer2::Copy2DTo


## -description


Copies the buffer to another 2D buffer object.


## -parameters




### -param pDestBuffer [in]

A pointer to the <a href="https://msdn.microsoft.com/BFA73B1A-F8A7-4100-9DBD-234CCA06F9F5">IMF2DBuffer2</a> interface of the destination buffer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The destination buffer must be at least as large as the source buffer.




## -see-also




<a href="https://msdn.microsoft.com/BFA73B1A-F8A7-4100-9DBD-234CCA06F9F5">IMF2DBuffer2</a>
 

 

