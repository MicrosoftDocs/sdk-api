---
UID: NS:vss._VSS_PROVIDER_PROP
title: "_VSS_PROVIDER_PROP"
author: windows-sdk-content
description: Specifies shadow copy provider properties.
old-location: base\vss_provider_prop.htm
old-project: vss
ms.assetid: 000da95d-a3f5-447e-a96d-c8fb34e9d0d3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PVSS_PROVIDER_PROP, PVSS_PROVIDER_PROP, PVSS_PROVIDER_PROP structure pointer [VSS], VSS_PROVIDER_PROP, VSS_PROVIDER_PROP structure [VSS], _VSS_PROVIDER_PROP, _win32_vss_provider_prop, base.vss_provider_prop, vss/PVSS_PROVIDER_PROP, vss/VSS_PROVIDER_PROP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: VSS_PROVIDER_PROP, *PVSS_PROVIDER_PROP
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

