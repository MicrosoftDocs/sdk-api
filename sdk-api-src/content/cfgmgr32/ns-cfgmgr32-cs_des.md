---
UID: NS:cfgmgr32.CS_Des_s
title: CS_DES (cfgmgr32.h)
description: The CS_DES structure is used for specifying a resource list that describes device class-specific resource usage for a device instance. For more information about resource lists, see Hardware Resources.
helpviewer_keywords: ["*PCS_DES","CS_DES","CS_DES structure [Device and Driver Installation]","PCS_DES","PCS_DES structure pointer [Device and Driver Installation]","cfgmgr32/CS_DES","cfgmgr32/PCS_DES","cfgmgrst_b22826b5-3488-4667-831a-24b848f2dd74.xml","devinst.cs_des"]
old-location: devinst\cs_des.htm
tech.root: devinst
ms.assetid: 16b47fe9-cb84-453d-b515-bfdba254f947
ms.date: 12/05/2018
ms.keywords: '*PCS_DES, CS_DES, CS_DES structure [Device and Driver Installation], PCS_DES, PCS_DES structure pointer [Device and Driver Installation], cfgmgr32/CS_DES, cfgmgr32/PCS_DES, cfgmgrst_b22826b5-3488-4667-831a-24b848f2dd74.xml, devinst.cs_des'
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CS_DES, *PCS_DES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CS_Des_s
 - cfgmgr32/CS_Des_s
 - PCS_DES
 - cfgmgr32/PCS_DES
 - CS_DES
 - cfgmgr32/CS_DES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - CS_DES
---

# CS_DES structure


## -description

The CS_DES structure is used for specifying a resource list that describes device class-specific resource usage for a device instance. For more information about resource lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field CSD_SignatureLength

The number of elements in the byte array specified by <b>CSD_Signature</b>.

### -field CSD_LegacyDataOffset

Offset, in bytes, from the beginning of the <b>CSD_Signature</b> array to the beginning of a block of data. For example, if the data block follows the signature array, and if the signature array length is 16 bytes, then the value for <b>CSD_LegacyDataOffset</b> should be 16.

### -field CSD_LegacyDataSize

Length, in bytes, of the data block whose offset is specified by <b>CSD_LegacyDataOffset</b>.

### -field CSD_Flags

<i>Not used.</i>

### -field CSD_ClassGuid

A globally unique identifier (GUID) identifying a <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a>. If both <b>CSD_SignatureLength</b> and <b>CSD_LegacyDataSize</b> are zero, the GUID is null.

### -field CSD_Signature

A byte array containing a class-specific signature.

## -remarks

The data block identified by <b>CSD_LegacyDataSize</b> and <b>CSD_LegacyDataOffset</b> can contain legacy, class-specific data, as stored in the <b>DeviceSpecificData</b> member of a <a href="/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor">CM_PARTIAL_RESOURCE_DESCRIPTOR</a> structure, if the structure's <b>Type</b> member is <b>CmResourceTypeDeviceSpecific</b>.

The class-specific signature identified by <b>CSD_SignatureLength</b> and <b>CSD_Signature</b> can contain additional class-specific device identification information.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor">CM_PARTIAL_RESOURCE_DESCRIPTOR</a>



[CS_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cs_resource)