---
UID: NS:vss._VSS_PROVIDER_PROP
title: VSS_PROVIDER_PROP (vss.h)
author: windows-sdk-content
description: Specifies shadow copy provider properties.
old-location: base\vss_provider_prop.htm
tech.root: VSS
ms.assetid: 000da95d-a3f5-447e-a96d-c8fb34e9d0d3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PVSS_PROVIDER_PROP, PVSS_PROVIDER_PROP, PVSS_PROVIDER_PROP structure pointer [VSS], VSS_PROVIDER_PROP, VSS_PROVIDER_PROP structure [VSS], _win32_vss_provider_prop, base.vss_provider_prop, vss/PVSS_PROVIDER_PROP, vss/VSS_PROVIDER_PROP'
ms.topic: struct
f1_keywords:
- vss/VSS_PROVIDER_PROP
req.header: vss.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vss.h
api_name:
- VSS_PROVIDER_PROP
product: Windows
targetos: Windows
req.typenames: VSS_PROVIDER_PROP, *PVSS_PROVIDER_PROP
req.redist: 
ms.custom: 19H1
---

# VSS_PROVIDER_PROP structure


## -description


The <b>VSS_PROVIDER_PROP</b> structure specifies 
    shadow copy provider properties.


## -struct-fields




### -field m_ProviderId

Identifies the provider who supports shadow copies of this class.


### -field m_pwszProviderName

Null-terminated wide character string containing the provider name.


### -field m_eProviderType

Provider type. See <a href="https://docs.microsoft.com/windows/desktop/api/vss/ne-vss-vss_provider_type">VSS_PROVIDER_TYPE</a> for more 
      information.


### -field m_pwszProviderVersion

Null-terminated wide character string containing the provider version in readable format.


### -field m_ProviderVersionId

A <a href="https://docs.microsoft.com/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a> (GUID) uniquely 
      identifying the version of a provider.


### -field m_ClassId

Class identifier of the component registered in the local machine's COM catalog.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vss/ne-vss-vss_provider_type">VSS_PROVIDER_TYPE</a>
 

 

