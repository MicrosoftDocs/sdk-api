---
UID: NF:mfapi.MFGetAttributeDouble
title: MFGetAttributeDouble function
author: windows-sdk-content
description: Returns a double value from an attribute store, or a default value if the attribute is not present.
old-location: mf\mfgetattributedouble.htm
old-project: medfound
ms.assetid: 61a9e327-da29-45fd-8a99-e341561826af
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 61a9e327-da29-45fd-8a99-e341561826af, MFGetAttributeDouble, MFGetAttributeDouble function [Media Foundation], mf.mfgetattributedouble, mfapi/MFGetAttributeDouble
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFGetAttributeDouble
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MFGetAttributeDouble function


## -description



Returns a <b>double</b> value from an attribute store, or a default value if the attribute is not present.




## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.


### -param guidKey [in]

GUID that identifies which value to retrieve.


### -param fDefault [in]

Default value to return if the attribute store does not contain the specified attribute.


## -returns



Returns a <b>double</b> value.




## -remarks



This helper function queries the attribute store for the attribute specified by <i>guidKey</i>. If the attribute is not present or does not have type <b>double</b>, the function returns <i>fDefault</i>.

This function is convenient because it never returns a failure code. However, if the attribute in question does not have a meaningful default value, you should call <a href="https://msdn.microsoft.com/650a5f7f-609f-477b-8834-ff66ca3a9ca3">IMFAttributes::GetDouble</a> and check for MF_E_ATTRIBUTENOTFOUND.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/650a5f7f-609f-477b-8834-ff66ca3a9ca3">IMFAttributes::GetDouble</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

