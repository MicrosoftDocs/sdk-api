---
UID: NF:xenroll.IEnroll.enumProvidersWStr
title: IEnroll::enumProvidersWStr
author: windows-sdk-content
description: The IEnroll4::enumProvidersWStr method retrieves the names of the available cryptographic service providers (CSPs) specified by the ProviderType property.
old-location: security\ienroll4_enumproviderswstr.htm
tech.root: seccrypto
ms.assetid: f3b40f56-3332-44e8-9753-4107948d0801
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IEnroll interface [Security],enumProvidersWStr method, IEnroll.enumProvidersWStr, IEnroll::enumProvidersWStr, enumProvidersWStr, enumProvidersWStr method [Security], enumProvidersWStr method [Security],IEnroll interface, security.ienroll4_enumproviderswstr, xenroll/IEnroll::enumProvidersWStr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.enumProvidersWStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::enumProvidersWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>enumProvidersWStr</b> method retrieves the names of the available <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> (CSPs) specified by the 
<a href="https://msdn.microsoft.com/d4ab2b0e-127f-4ec0-9e4a-4314561912e3">ProviderType</a> property. This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.


## -parameters




### -param dwIndex [in]

Specifies the ordinal position of the CSP whose name will be retrieved. Specify zero for the first CSP.


### -param dwFlags [in]

Specifies flags that are passed through to the <a href="https://msdn.microsoft.com/2d93ef0f-b48f-481b-ba62-c535476fde08">CryptEnumProviders</a> function. Not currently used; specify zero.


### -param pbstrProvName [out]

A pointer to a <b>LPWSTR</b> variable that receives the name of a CSP with the specified property type.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. The value ERROR_NO_MORE_ITEMS is returned when there are no more CSPs with the property type indicated by the 
<a href="https://msdn.microsoft.com/d4ab2b0e-127f-4ec0-9e4a-4314561912e3">ProviderType</a> property.




## -remarks



If the 
<a href="https://msdn.microsoft.com/d4ab2b0e-127f-4ec0-9e4a-4314561912e3">ProviderType</a> property value has not been set, the default value (usually PROV_RSA_FULL) of <b>ProviderType</b> as set in the registry is used.

The <b>enumProvidersWStr</b> method  calls the 
<a href="https://msdn.microsoft.com/2d93ef0f-b48f-481b-ba62-c535476fde08">CryptEnumProviders</a> function.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

