---
UID: NF:mfapi.MFGetAttributeUINT32
title: MFGetAttributeUINT32 function
author: windows-sdk-content
description: Returns a UINT32 value from an attribute store, or a default value if the attribute is not present.
old-location: mf\mfgetattributeuint32.htm
tech.root: MedFound
ms.assetid: b79f3b2c-6293-41b2-afe7-4a0b2c27b34f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MFGetAttributeUINT32, MFGetAttributeUINT32 function [Media Foundation], b79f3b2c-6293-41b2-afe7-4a0b2c27b34f, mf.mfgetattributeuint32, mfapi/MFGetAttributeUINT32
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MFGetAttributeUINT32
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFGetAttributeUINT32 function


## -description



Returns a <b>UINT32</b> value from an attribute store, or a default value if the attribute is not present.




## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.


### -param guidKey [in]

GUID that identifies which value to retrieve.


### -param unDefault [in]

Default value to return if the attribute store does not contain the specified attribute.


## -returns



Returns a <b>UINT32</b> value.




## -remarks



This helper function queries the attribute store for the <b>UINT32</b> value specified by <i>guidKey</i>. If the value is not present or does not have type <b>UINT32</b>, the function returns <i>unDefault</i>.

This function is convenient because it never returns a failure code. However, if the attribute in question does not have a meaningful default value, you should call <a href="https://msdn.microsoft.com/e47495e0-3274-4ce2-9fd3-d2fb2afb7578">IMFAttributes::GetUINT32</a> and check for MF_E_ATTRIBUTENOTFOUND.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e47495e0-3274-4ce2-9fd3-d2fb2afb7578">IMFAttributes::GetUINT32</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

