---
UID: NF:mfapi.MFGetAttributeString
title: MFGetAttributeString function
author: windows-sdk-content
description: Gets a string value from an attribute store.
old-location: mf\mfgetattributestring.htm
old-project: medfound
ms.assetid: 6CA416AB-5EA1-4A85-A421-1CDD3D111296
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFGetAttributeString, MFGetAttributeString function [Media Foundation], mf.mfgetattributestring, mfapi/MFGetAttributeString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfapi.h
api_name:
-	MFGetAttributeString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MFGetAttributeString function


## -description


Gets a string value from an attribute store.


## -parameters




### -param pAttributes [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface.


### -param guidKey [in]

A GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_STRING</b>. 



### -param ppsz [out]

If the key is found and the value is a string type, this parameter receives a copy of the string. The caller must free the memory for the string by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. 



## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is a wrapper for the <a href="https://msdn.microsoft.com/550a3035-ea16-4784-8f69-9522259bb338">IMFAttributes::GetAllocatedString</a> method.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

