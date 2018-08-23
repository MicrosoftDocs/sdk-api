---
UID: NE:faxcomex.FAX_RULE_STATUS_ENUM
title: FAX_RULE_STATUS_ENUM
author: windows-sdk-content
description: The FAX_RULE_STATUS_ENUM enumeration defines the status types for outbound routing rules.
old-location: fax\_mfax_fax_rule_status_enum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5p2l.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FAX_RULE_STATUS_ENUM, FAX_RULE_STATUS_ENUM enumeration [Fax Service], _mfax_fax_rule_status_enum, fax._mfax_fax_rule_status_enum, faxcomex/FAX_RULE_STATUS_ENUM, faxcomex/frsALL_GROUP_DEV_NOT_VALID, faxcomex/frsBAD_DEVICE, faxcomex/frsEMPTY_GROUP, faxcomex/frsSOME_GROUP_DEV_NOT_VALID, faxcomex/frsVALID, frsALL_GROUP_DEV_NOT_VALID, frsBAD_DEVICE, frsEMPTY_GROUP, frsSOME_GROUP_DEV_NOT_VALID, frsVALID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: faxcomex.h
req.include-header: 
req.redist: 
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
req.typenames: FAX_RULE_STATUS_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_RULE_STATUS_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# FAX_RULE_STATUS_ENUM enumeration


## -description


The <b>FAX_RULE_STATUS_ENUM</b> enumeration defines the status types for outbound routing rules.


## -enum-fields




### -field frsVALID

The routing rule is valid and can be applied to outbound faxes.


### -field frsEMPTY_GROUP

The routing rule cannot be applied because the rule uses an outbound routing group for its destination and the group is empty.


### -field frsALL_GROUP_DEV_NOT_VALID

The routing rule cannot be applied because the rule uses an existing outbound routing group for its destination and the group does not contain devices that are valid for sending faxes.


### -field frsSOME_GROUP_DEV_NOT_VALID

The routing rule uses an existing outbound routing group for its destination but the group contains devices that are not valid for sending faxes.



This is a warning status. The rule can be applied to the valid devices in the routing group.



### -field frsBAD_DEVICE

The routing rule cannot be applied because the rule uses a single device for its destination and that device is not valid for sending faxes.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689593(v=VS.85).aspx">IFaxOutboundRoutingRule::get_Status</a>
 

 

