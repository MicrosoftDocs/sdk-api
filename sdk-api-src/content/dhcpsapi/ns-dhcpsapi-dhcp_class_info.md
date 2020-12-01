---
UID: NS:dhcpsapi._DHCP_CLASS_INFO
title: DHCP_CLASS_INFO (dhcpsapi.h)
description: Defines a DHCP option class.
helpviewer_keywords: ["*LPDHCP_CLASS_INFO","DHCP_CLASS_INFO","DHCP_CLASS_INFO structure [DHCP]","DHCP_FLAGS_OPTION_IS_VENDOR","LPDHCP_CLASS_INFO","LPDHCP_CLASS_INFO structure pointer [DHCP]","dhcp.dhcp_class_info","dhcpsapi/LPDHCP_CLASS_INFO","dhcpsapi/_DHCP_CLASS_INFO"]
old-location: dhcp\dhcp_class_info.htm
tech.root: DHCP
ms.assetid: 62fb9f21-ad21-4525-90f4-48dc5a8b230b
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLASS_INFO, DHCP_CLASS_INFO, DHCP_CLASS_INFO structure [DHCP], DHCP_FLAGS_OPTION_IS_VENDOR, LPDHCP_CLASS_INFO, LPDHCP_CLASS_INFO structure pointer [DHCP], dhcp.dhcp_class_info, dhcpsapi/LPDHCP_CLASS_INFO, dhcpsapi/_DHCP_CLASS_INFO'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: DHCP_CLASS_INFO, *LPDHCP_CLASS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLASS_INFO
 - dhcpsapi/_DHCP_CLASS_INFO
 - LPDHCP_CLASS_INFO
 - dhcpsapi/LPDHCP_CLASS_INFO
 - DHCP_CLASS_INFO
 - dhcpsapi/DHCP_CLASS_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_CLASS_INFO
---

# DHCP_CLASS_INFO structure


## -description

The <b>DHCP_CLASS_INFO</b> structure defines a DHCP option class.

## -struct-fields

### -field ClassName

Unicode string that contains the name of the class.

### -field ClassComment

Unicode string that contains a comment associated with the class.

### -field ClassDataLength

Specifies the size of <b>ClassData</b>, in bytes. When passing this structure into <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetclassinfo">DhcpGetClassInfo</a>, this value should be set to the size of the initialized buffer.

### -field IsVendor

Specifies whether or not this option class is a vendor-defined option class. If <b>TRUE</b>, it is a vendor class; if not, it is not a vendor class. Vendor-defined option classes can be used by DHCP clients that are configured to optionally identify themselves by their vendor type to the DHCP server when obtaining a lease.

### -field Flags

Specifies a bit flag that indicates whether or not the options are vendor-specific. If it is not, this parameter should be 0.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
</dl>
</td>
<td width="60%">
This flag should be set if the option is provided by a vendor.

</td>
</tr>
</table>

### -field ClassData

Pointer to a byte buffer that contains specific data for the class. When passing this structure into <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetclassinfo">DhcpGetClassInfo</a>, this buffer should be initialized to the anticipated size of the data to be returned.

### -field ClassData.size_is

### -field ClassData.size_is.ClassDataLength

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info_array">DHCP_CLASS_INFO_ARRAY</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateclass">DhcpCreateClass</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetclassinfo">DhcpGetClassInfo</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpmodifyclass">DhcpModifyClass</a>