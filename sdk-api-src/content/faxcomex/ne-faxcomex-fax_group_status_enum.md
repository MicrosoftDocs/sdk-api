---
UID: NE:faxcomex.FAX_GROUP_STATUS_ENUM
title: FAX_GROUP_STATUS_ENUM
author: windows-sdk-content
description: The FAX_GROUP_STATUS_ENUM enumeration defines the status types for outbound routing groups.
old-location: fax\_mfax_fax_group_status_enum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0tyl.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FAX_GROUP_STATUS_ENUM, FAX_GROUP_STATUS_ENUM enumeration [Fax Service], _mfax_fax_group_status_enum, fax._mfax_fax_group_status_enum, faxcomex/FAX_GROUP_STATUS_ENUM, faxcomex/fgsALL_DEV_NOT_VALID, faxcomex/fgsALL_DEV_VALID, faxcomex/fgsEMPTY, faxcomex/fgsSOME_DEV_NOT_VALID, fgsALL_DEV_NOT_VALID, fgsALL_DEV_VALID, fgsEMPTY, fgsSOME_DEV_NOT_VALID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: FAX_GROUP_STATUS_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_GROUP_STATUS_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# FAX_GROUP_STATUS_ENUM enumeration


## -description


The <b>FAX_GROUP_STATUS_ENUM</b> enumeration defines the status types for outbound routing groups.


## -enum-fields




### -field fgsALL_DEV_VALID

All the devices in the routing group are valid and available for sending outgoing faxes.


### -field fgsEMPTY

The routing group does not contain any devices.


### -field fgsALL_DEV_NOT_VALID

The routing group does not contain any available devices for sending faxes. (Devices can be "unavailable" when they are offline and when they do not exist.)


### -field fgsSOME_DEV_NOT_VALID

The routing group contains some devices that are unavailable for sending faxes. (Devices can be "unavailable" when they are offline and when they do not exist.)


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms688419(v=VS.85).aspx">IFaxOutboundRoutingGroup::get_Status</a>
 

 

