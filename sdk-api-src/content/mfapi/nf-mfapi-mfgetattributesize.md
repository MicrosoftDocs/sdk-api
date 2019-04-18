---
UID: NF:mfapi.MFGetAttributeSize
title: MFGetAttributeSize function (mfapi.h)
author: windows-sdk-content
description: Retrieves an attribute whose value is a size, expressed as a width and height.
old-location: mf\mfgetattributesize.htm
tech.root: medfound
ms.assetid: c74445b2-a2ec-4c77-a8bf-61a6b54cef75
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFGetAttributeSize, MFGetAttributeSize function [Media Foundation], c74445b2-a2ec-4c77-a8bf-61a6b54cef75, mf.mfgetattributesize, mfapi/MFGetAttributeSize
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
 - MFGetAttributeSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFGetAttributeSize function


## -description



Retrieves an attribute whose value is a size, expressed as a width and height.




## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.


### -param guidKey [in]

<b>GUID</b> that identifies which value to retrieve. The attribute type must be MF_ATTRIBUTE_UINT64.


### -param punWidth [out]

Receives the width.


### -param punHeight [out]

Receives the height.


## -returns



This function can return one of these values.




## -remarks



Some attributes specify a size as a packed <b>UINT64</b> value. Use this function to get the numerator and denominator as separate 32-bit values.




## -see-also




<a href="https://msdn.microsoft.com/cf7b3cfe-fdce-417d-8c0b-198d026b8768">MFSetAttributeSize</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

