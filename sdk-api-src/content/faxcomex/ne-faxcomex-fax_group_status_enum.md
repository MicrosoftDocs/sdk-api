---
UID: NE:faxcomex.FAX_GROUP_STATUS_ENUM
title: FAX_GROUP_STATUS_ENUM (faxcomex.h)
description: The FAX_GROUP_STATUS_ENUM enumeration defines the status types for outbound routing groups.
helpviewer_keywords: ["FAX_GROUP_STATUS_ENUM","FAX_GROUP_STATUS_ENUM enumeration [Fax Service]","_mfax_fax_group_status_enum","fax._mfax_fax_group_status_enum","faxcomex/FAX_GROUP_STATUS_ENUM","faxcomex/fgsALL_DEV_NOT_VALID","faxcomex/fgsALL_DEV_VALID","faxcomex/fgsEMPTY","faxcomex/fgsSOME_DEV_NOT_VALID","fgsALL_DEV_NOT_VALID","fgsALL_DEV_VALID","fgsEMPTY","fgsSOME_DEV_NOT_VALID"]
old-location: fax\_mfax_fax_group_status_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0tyl.htm
ms.date: 12/05/2018
ms.keywords: FAX_GROUP_STATUS_ENUM, FAX_GROUP_STATUS_ENUM enumeration [Fax Service], _mfax_fax_group_status_enum, fax._mfax_fax_group_status_enum, faxcomex/FAX_GROUP_STATUS_ENUM, faxcomex/fgsALL_DEV_NOT_VALID, faxcomex/fgsALL_DEV_VALID, faxcomex/fgsEMPTY, faxcomex/fgsSOME_DEV_NOT_VALID, fgsALL_DEV_NOT_VALID, fgsALL_DEV_VALID, fgsEMPTY, fgsSOME_DEV_NOT_VALID
req.header: faxcomex.h
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
targetos: Windows
req.typenames: FAX_GROUP_STATUS_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_GROUP_STATUS_ENUM
 - faxcomex/FAX_GROUP_STATUS_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_GROUP_STATUS_ENUM
---

# FAX_GROUP_STATUS_ENUM enumeration


## -description

The <b>FAX_GROUP_STATUS_ENUM</b> enumeration defines the status types for outbound routing groups.

## -enum-fields

### -field fgsALL_DEV_VALID:0

All the devices in the routing group are valid and available for sending outgoing faxes.

### -field fgsEMPTY

The routing group does not contain any devices.

### -field fgsALL_DEV_NOT_VALID

The routing group does not contain any available devices for sending faxes. (Devices can be "unavailable" when they are offline and when they do not exist.)

### -field fgsSOME_DEV_NOT_VALID

The routing group contains some devices that are unavailable for sending faxes. (Devices can be "unavailable" when they are offline and when they do not exist.)

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroup-status-vb">IFaxOutboundRoutingGroup::get_Status</a>
