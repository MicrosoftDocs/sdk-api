---
UID: NS:winbio_adapter._WINBIO_ADAPTER_INTERFACE_VERSION
title: WINBIO_ADAPTER_INTERFACE_VERSION (winbio_adapter.h)
description: Contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.
helpviewer_keywords: ["*PWINBIO_ADAPTER_INTERFACE_VERSION","PWINBIO_ADAPTER_INTERFACE_VERSION","PWINBIO_ADAPTER_INTERFACE_VERSION structure pointer [Windows Biometric Framework API]","WINBIO_ADAPTER_INTERFACE_VERSION","WINBIO_ADAPTER_INTERFACE_VERSION structure [Windows Biometric Framework API]","secbiomet.winbio_adapter_interface_version","winbio_adapter/PWINBIO_ADAPTER_INTERFACE_VERSION","winbio_adapter/WINBIO_ADAPTER_INTERFACE_VERSION"]
old-location: secbiomet\winbio_adapter_interface_version.htm
tech.root: SecBioMet
ms.assetid: e9dd91ea-cca3-49f3-89dc-f8f2c0594bd2
ms.date: 12/05/2018
ms.keywords: '*PWINBIO_ADAPTER_INTERFACE_VERSION, PWINBIO_ADAPTER_INTERFACE_VERSION, PWINBIO_ADAPTER_INTERFACE_VERSION structure pointer [Windows Biometric Framework API], WINBIO_ADAPTER_INTERFACE_VERSION, WINBIO_ADAPTER_INTERFACE_VERSION structure [Windows Biometric Framework API], secbiomet.winbio_adapter_interface_version, winbio_adapter/PWINBIO_ADAPTER_INTERFACE_VERSION, winbio_adapter/WINBIO_ADAPTER_INTERFACE_VERSION'
req.header: winbio_adapter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: WINBIO_ADAPTER_INTERFACE_VERSION, *PWINBIO_ADAPTER_INTERFACE_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINBIO_ADAPTER_INTERFACE_VERSION
 - winbio_adapter/_WINBIO_ADAPTER_INTERFACE_VERSION
 - PWINBIO_ADAPTER_INTERFACE_VERSION
 - winbio_adapter/PWINBIO_ADAPTER_INTERFACE_VERSION
 - WINBIO_ADAPTER_INTERFACE_VERSION
 - winbio_adapter/WINBIO_ADAPTER_INTERFACE_VERSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio_adapter.h
api_name:
 - WINBIO_ADAPTER_INTERFACE_VERSION
---

# WINBIO_ADAPTER_INTERFACE_VERSION structure


## -description

The <b>WINBIO_ADAPTER_INTERFACE_VERSION</b> structure contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.

## -struct-fields

### -field MajorVersion

Contains the major version number.

### -field MinorVersion

Contains the minor version number.

## -remarks

This structure is used by the following structures:

<ul>
<li>
<a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_engine_interface">WINBIO_ENGINE_INTERFACE</a>
</li>
<li>
<a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_sensor_interface">WINBIO_SENSOR_INTERFACE</a>
</li>
<li>
<a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_storage_interface">WINBIO_STORAGE_INTERFACE</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/SecBioMet/plug-in-structures">Plug-in Structures</a>