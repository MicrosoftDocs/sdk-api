---
UID: NS:winbio_adapter._WINBIO_ADAPTER_INTERFACE_VERSION
title: WINBIO_ADAPTER_INTERFACE_VERSION
author: windows-sdk-content
description: Contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.
old-location: secbiomet\winbio_adapter_interface_version.htm
tech.root: SecBioMet
ms.assetid: e9dd91ea-cca3-49f3-89dc-f8f2c0594bd2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWINBIO_ADAPTER_INTERFACE_VERSION, PWINBIO_ADAPTER_INTERFACE_VERSION, PWINBIO_ADAPTER_INTERFACE_VERSION structure pointer [Windows Biometric Framework API], WINBIO_ADAPTER_INTERFACE_VERSION, WINBIO_ADAPTER_INTERFACE_VERSION structure [Windows Biometric Framework API], secbiomet.winbio_adapter_interface_version, winbio_adapter/PWINBIO_ADAPTER_INTERFACE_VERSION, winbio_adapter/WINBIO_ADAPTER_INTERFACE_VERSION"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio_adapter.h
api_name:
 - WINBIO_ADAPTER_INTERFACE_VERSION
product: Windows
targetos: Windows
req.typenames: WINBIO_ADAPTER_INTERFACE_VERSION, *PWINBIO_ADAPTER_INTERFACE_VERSION
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Dd401655(v=VS.85).aspx">WINBIO_ENGINE_INTERFACE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd401660(v=VS.85).aspx">WINBIO_SENSOR_INTERFACE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd401661(v=VS.85).aspx">WINBIO_STORAGE_INTERFACE</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/64fb908c-72c2-4639-a2f6-77ede080512c">Plug-in Structures</a>
 

 

