---
UID: NF:mfapi.MFGetAttributeUINT64
title: MFGetAttributeUINT64 function
author: windows-sdk-content
description: Returns a UINT64 value from an attribute store, or a default value if the attribute is not present.
old-location: mf\mfgetattributeuint64.htm
tech.root: medfound
ms.assetid: 843946a4-d270-4440-9818-59e95cbf9a5b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 843946a4-d270-4440-9818-59e95cbf9a5b, MFGetAttributeUINT64, MFGetAttributeUINT64 function [Media Foundation], mf.mfgetattributeuint64, mfapi/MFGetAttributeUINT64
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
 - MFGetAttributeUINT64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFGetAttributeUINT64 function


## -description



Returns a <b>UINT64</b> value from an attribute store, or a default value if the attribute is not present.




## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.


### -param guidKey [in]

GUID that identifies which value to retrieve.


### -param unDefault [in]

Default value to return if the attribute store does not contain the specified attribute.


## -returns



Returns a <b>UINT64</b> value.




## -remarks



This helper function queries the attribute store for the <b>UINT64</b> value specified by guidKey. If the value is not present, the function returns <i>unDefault</i>.

This function is convenient because it never returns a failure code. However, if the attribute in question does not have a meaningful default value, you should call <a href="https://msdn.microsoft.com/f3240fff-48d8-4d88-8c75-15f00bfe72ed">IMFAttributes::GetUINT64</a> and check for MF_E_ATTRIBUTENOTFOUND.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/f3240fff-48d8-4d88-8c75-15f00bfe72ed">IMFAttributes::GetUINT64</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

