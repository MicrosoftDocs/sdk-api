---
UID: NS:wcndevice.tagWCN_VENDOR_EXTENSION_SPEC
title: WCN_VENDOR_EXTENSION_SPEC (wcndevice.h)
description: WCN_VENDOR_EXTENSION_SPEC structure contains data that defines a vendor extension.
helpviewer_keywords: ["PWCN_VENDOR_EXTENSION_SPEC","PWCN_VENDOR_EXTENSION_SPEC structure pointer [Windows Connect Now]","WCN_FLAG_AUTHENTICATED_VE","WCN_FLAG_DISCOVERY_VE","WCN_FLAG_ENCRYPTED_VE","WCN_VENDOR_EXTENSION_SPEC","WCN_VENDOR_EXTENSION_SPEC structure [Windows Connect Now]","wcn.wcn_vendor_extension_spec","wcndevice/PWCN_VENDOR_EXTENSION_SPEC","wcndevice/WCN_VENDOR_EXTENSION_SPEC"]
old-location: wcn\wcn_vendor_extension_spec.htm
tech.root: wcn
ms.assetid: 8ba35c4a-a644-4c6d-8334-d459e7196b6f
ms.date: 12/05/2018
ms.keywords: PWCN_VENDOR_EXTENSION_SPEC, PWCN_VENDOR_EXTENSION_SPEC structure pointer [Windows Connect Now], WCN_FLAG_AUTHENTICATED_VE, WCN_FLAG_DISCOVERY_VE, WCN_FLAG_ENCRYPTED_VE, WCN_VENDOR_EXTENSION_SPEC, WCN_VENDOR_EXTENSION_SPEC structure [Windows Connect Now], wcn.wcn_vendor_extension_spec, wcndevice/PWCN_VENDOR_EXTENSION_SPEC, wcndevice/WCN_VENDOR_EXTENSION_SPEC
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wcndevice.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WCN_VENDOR_EXTENSION_SPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWCN_VENDOR_EXTENSION_SPEC
 - wcndevice/tagWCN_VENDOR_EXTENSION_SPEC
 - WCN_VENDOR_EXTENSION_SPEC
 - wcndevice/WCN_VENDOR_EXTENSION_SPEC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcndevice.h
api_name:
 - WCN_VENDOR_EXTENSION_SPEC
---

# WCN_VENDOR_EXTENSION_SPEC structure


## -description

The <b>WCN_VENDOR_EXTENSION_SPEC</b> structure contains data that defines a vendor extension.

## -struct-fields

### -field VendorId

Set this value to the SMI Enterprise ID Number of the vendor that defines the vendor extension. For example, the Microsoft ID is '311' (WCN_MICROSOFT_VENDOR_ID).

### -field SubType

The subtype, as defined by the first two bytes of the vendor extension. If the vendor has  not provided the two-byte subtype prefix, use WCN_NO_SUBTYPE.

### -field Index

Distinguishes between multiple vendor extensions with the same VendorID and SubType. The index begins at zero.

### -field Flags

Applications must specify one of the following flag values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WCN_FLAG_DISCOVERY_VE"></a><a id="wcn_flag_discovery_ve"></a><dl>
<dt><b>WCN_FLAG_DISCOVERY_VE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The vendor extension was not available  before the session started. The vendor extension is not secure.

</td>
</tr>
<tr>
<td width="40%"><a id="WCN_FLAG_AUTHENTICATED_VE"></a><a id="wcn_flag_authenticated_ve"></a><dl>
<dt><b>WCN_FLAG_AUTHENTICATED_VE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The vendor extension is authentic. Only devices that pass authentication can read or write authenticated vendor extensions.

</td>
</tr>
<tr>
<td width="40%"><a id="WCN_FLAG_ENCRYPTED_VE"></a><a id="wcn_flag_encrypted_ve"></a><dl>
<dt><b>WCN_FLAG_ENCRYPTED_VE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The vendor extension is authentic and encrypted. In addition to the guarantee of authenticated vendor extensions, vendor extensions are encrypted before transmission.

</td>
</tr>
</table>

