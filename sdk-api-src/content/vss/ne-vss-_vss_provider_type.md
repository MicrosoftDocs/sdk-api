---
UID: NE:vss._VSS_PROVIDER_TYPE
title: "_VSS_PROVIDER_TYPE"
author: windows-sdk-content
description: Specifies the provider type.
old-location: base\vss_provider_type.htm
old-project: VSS
ms.assetid: 76a85ff4-df3c-4280-a6f1-2a1cff96ccfd
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PVSS_PROVIDER_TYPE, PVSS_PROVIDER_TYPE, PVSS_PROVIDER_TYPE enumeration pointer [VSS], VSS_PROVIDER_TYPE, VSS_PROVIDER_TYPE enumeration [VSS], VSS_PROV_FILESHARE, VSS_PROV_HARDWARE, VSS_PROV_SOFTWARE, VSS_PROV_SYSTEM, VSS_PROV_UNKNOWN, _VSS_PROVIDER_TYPE, _win32_vss_provider_type, base.vss_provider_type, vss/PVSS_PROVIDER_TYPE, vss/VSS_PROVIDER_TYPE, vss/VSS_PROV_FILESHARE, vss/VSS_PROV_HARDWARE, vss/VSS_PROV_SOFTWARE, vss/VSS_PROV_SYSTEM, vss/VSS_PROV_UNKNOWN"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: VSS_PROVIDER_TYPE, *PVSS_PROVIDER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vss.h
api_name:
-	VSS_PROVIDER_TYPE
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VSS_PROVIDER_TYPE enumeration


## -description


The <b>VSS_PROVIDER_TYPE</b> enumeration specifies 
    the provider type.


## -enum-fields




### -field VSS_PROV_UNKNOWN

The provider type is unknown. 
     

This indicates an error in the application or the VSS service, or that no provider is available.


### -field VSS_PROV_SYSTEM

The default provider that ships with Windows.


### -field VSS_PROV_SOFTWARE

A software provider.


### -field VSS_PROV_HARDWARE

A hardware provider.


### -field VSS_PROV_FILESHARE

A file share provider.

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>This enumeration value is not supported until Windows 8 and Windows Server 2012.


## -see-also




<a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">IVssBackupComponents::Query</a>



<a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a>



<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>



<a href="https://msdn.microsoft.com/e8d70f20-00a9-4cae-a92c-e3f3673a8db3">VSS_OBJECT_UNION</a>



<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_PROVIDER_PROP</a>



<a href="https://msdn.microsoft.com/cb89c3cc-5a8e-419e-839c-f72a1886eadf">VSS_SOURCE_TYPE</a>
 

 

