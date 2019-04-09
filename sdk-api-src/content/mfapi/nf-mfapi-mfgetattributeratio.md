---
UID: NF:mfapi.MFGetAttributeRatio
title: MFGetAttributeRatio function (mfapi.h)
author: windows-sdk-content
description: Retrieves an attribute whose value is a ratio.
old-location: mf\mfgetattributeratio.htm
tech.root: medfound
ms.assetid: 2572c30c-4ae1-42b7-b1f7-6c564d936c60
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 2572c30c-4ae1-42b7-b1f7-6c564d936c60, MFGetAttributeRatio, MFGetAttributeRatio function [Media Foundation], mf.mfgetattributeratio, mfapi/MFGetAttributeRatio
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
 - MFGetAttributeRatio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFGetAttributeRatio function


## -description



Retrieves an attribute whose value is a ratio.




## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.


### -param guidKey [in]

<b>GUID</b> that identifies which value to retrieve. The attribute type must be MF_ATTRIBUTE_UINT64.


### -param punNumerator [out]

Receives the numerator of the ratio.


### -param punDenominator [out]

Receives the denominator of the ratio.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Some attributes specify a ratio as a packed <b>UINT64</b> value. Use this function to get the numerator and denominator as separate 32-bit values.




## -see-also




<a href="https://msdn.microsoft.com/04e8c89e-115e-41d4-b8cb-953f68ddd14e">MFSetAttributeRatio</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

