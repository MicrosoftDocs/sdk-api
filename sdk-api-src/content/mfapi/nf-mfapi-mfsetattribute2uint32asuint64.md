---
UID: NF:mfapi.MFSetAttribute2UINT32asUINT64
title: MFSetAttribute2UINT32asUINT64 function
author: windows-sdk-content
description: Packs two UINT32 values into a UINT64 attribute value.
old-location: mf\mfsetattribute2uint32asuint64.htm
tech.root: medfound
ms.assetid: a9c64e49-e249-49ce-8d58-109a7f247fe9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFSetAttribute2UINT32asUINT64, MFSetAttribute2UINT32asUINT64 function [Media Foundation], mf.mfsetattribute2uint32asuint64, mfobjects/MFSetAttribute2UINT32asUINT64
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: Mfapi.h
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
 - mfobjects.h
api_name:
 - MFSetAttribute2UINT32asUINT64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFSetAttribute2UINT32asUINT64 function


## -description


Packs two <b>UINT32</b> values into a <b>UINT64</b> attribute value.


## -parameters




### -param pAttributes [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.




### -param guidKey [in]

A <b>GUID</b> that identifies the value to set. If this key already exists, the function overwrites the old value.




### -param unHigh32 [in]

The value to store in the high-order 32 bits of the <b>UINT64</b> value.




### -param unLow32 [in]

The value to store in the low-order 32 bits of the <b>UINT64</b> value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Internally, this functions calls <a href="https://msdn.microsoft.com/82d37211-e2e5-4b34-8102-2c3f8650cc26">Pack2UINT32AsUINT64</a> to create the 64-bit value, and <a href="https://msdn.microsoft.com/817ed1c1-16ad-4520-a1a0-a93563936b50">IMFAttributes::SetUINT64</a> to set the attribute.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

