---
UID: NE:vss._VSS_PROVIDER_TYPE
title: VSS_PROVIDER_TYPE (vss.h)
author: windows-sdk-content
description: Specifies the provider type.
old-location: base\vss_provider_type.htm
tech.root: VSS
ms.assetid: 76a85ff4-df3c-4280-a6f1-2a1cff96ccfd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PVSS_PROVIDER_TYPE, PVSS_PROVIDER_TYPE, PVSS_PROVIDER_TYPE enumeration pointer [VSS], VSS_PROVIDER_TYPE, VSS_PROVIDER_TYPE enumeration [VSS], VSS_PROV_FILESHARE, VSS_PROV_HARDWARE, VSS_PROV_SOFTWARE, VSS_PROV_SYSTEM, VSS_PROV_UNKNOWN, _win32_vss_provider_type, base.vss_provider_type, vss/PVSS_PROVIDER_TYPE, vss/VSS_PROVIDER_TYPE, vss/VSS_PROV_FILESHARE, vss/VSS_PROV_HARDWARE, vss/VSS_PROV_SOFTWARE, vss/VSS_PROV_SYSTEM, vss/VSS_PROV_UNKNOWN"
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
 - VSS_PROVIDER_TYPE
product: Windows
targetos: Windows
req.typenames: VSS_PROVIDER_TYPE, *PVSS_PROVIDER_TYPE
req.redist: 
ms.custom: 19H1
---

# VSS_PROVIDER_TYPE enumeration


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




<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">IVssBackupComponents::Query</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vss/nn-vss-ivssenumobject">IVssEnumObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001">VSS_OBJECT_UNION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_object_prop">VSS_PROVIDER_PROP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/ne-vswriter-vss_source_type">VSS_SOURCE_TYPE</a>
 

 

