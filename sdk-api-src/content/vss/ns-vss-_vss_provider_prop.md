---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _VSS_PROVIDER_PROP structure


## -description


The <b>VSS_PROVIDER_PROP</b> structure specifies 
    shadow copy provider properties.


## -struct-fields




### -field m_ProviderId

Identifies the provider who supports shadow copies of this class.


### -field m_pwszProviderName

Null-terminated wide character string containing the provider name.


### -field m_eProviderType

Provider type. See <a href="https://msdn.microsoft.com/76a85ff4-df3c-4280-a6f1-2a1cff96ccfd">VSS_PROVIDER_TYPE</a> for more 
      information.


### -field m_pwszProviderVersion

Null-terminated wide character string containing the provider version in readable format.


### -field m_ProviderVersionId

A <a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a> (GUID) uniquely 
      identifying the version of a provider.


### -field m_ClassId

Class identifier of the component registered in the local machine's COM catalog.


## -see-also




<a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a>



<a href="https://msdn.microsoft.com/76a85ff4-df3c-4280-a6f1-2a1cff96ccfd">VSS_PROVIDER_TYPE</a>
 

 

