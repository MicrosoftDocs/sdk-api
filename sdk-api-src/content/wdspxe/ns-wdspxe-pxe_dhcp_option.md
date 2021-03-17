---
UID: NS:wdspxe.tagPXE_DHCP_OPTION
title: PXE_DHCP_OPTION (wdspxe.h)
description: The PXE_DHCP_OPTION structure can be used with the Windows Deployment Services PXE Server API.
helpviewer_keywords: ["*PPXE_DHCP_OPTION","PPXE_DHCP_OPTION","PPXE_DHCP_OPTION structure pointer [Windows Deployment Services]","PXE_DHCP_OPTION","PXE_DHCP_OPTION structure [Windows Deployment Services]","wds.pxe_dhcp_option","wdspxe/PPXE_DHCP_OPTION","wdspxe/PXE_DHCP_OPTION"]
old-location: wds\pxe_dhcp_option.htm
tech.root: wds
ms.assetid: 3acc7641-07aa-4a95-a31c-74b48a749f5a
ms.date: 12/05/2018
ms.keywords: '*PPXE_DHCP_OPTION, PPXE_DHCP_OPTION, PPXE_DHCP_OPTION structure pointer [Windows Deployment Services], PXE_DHCP_OPTION, PXE_DHCP_OPTION structure [Windows Deployment Services], wds.pxe_dhcp_option, wdspxe/PPXE_DHCP_OPTION, wdspxe/PXE_DHCP_OPTION'
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
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
req.typenames: PXE_DHCP_OPTION, *PPXE_DHCP_OPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPXE_DHCP_OPTION
 - wdspxe/tagPXE_DHCP_OPTION
 - PPXE_DHCP_OPTION
 - wdspxe/PPXE_DHCP_OPTION
 - PXE_DHCP_OPTION
 - wdspxe/PXE_DHCP_OPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WdsPxe.h
api_name:
 - PXE_DHCP_OPTION
---

# PXE_DHCP_OPTION structure


## -description

The <b>PXE_DHCP_OPTION</b> structure can be used with the Windows Deployment Services PXE Server API.

## -struct-fields

### -field OptionType

A DHCP option type.

### -field OptionLength

Length of the option value.

### -field OptionValue

The option value.

