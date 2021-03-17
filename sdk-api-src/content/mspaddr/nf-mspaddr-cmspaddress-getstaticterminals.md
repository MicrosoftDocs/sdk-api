---
UID: NF:mspaddr.CMSPAddress.GetStaticTerminals
title: CMSPAddress::GetStaticTerminals (mspaddr.h)
description: The GetStaticTerminals method is called by our wrapper methods ( get_StaticTerminals and EnumerateStaticTerminals) to get an array of static terminals that can be used on this address.
helpviewer_keywords: ["CMSPAddress interface [TAPI 2.2]","GetStaticTerminals method","CMSPAddress.GetStaticTerminals","CMSPAddress::GetStaticTerminals","GetStaticTerminals","GetStaticTerminals method [TAPI 2.2]","GetStaticTerminals method [TAPI 2.2]","CMSPAddress interface","_tapi3_cmspaddress_getstaticterminals","mspaddr/CMSPAddress::GetStaticTerminals","tapi3.cmspaddress_getstaticterminals"]
old-location: tapi3\cmspaddress_getstaticterminals.htm
tech.root: tapi3
ms.assetid: 8fffc00d-a783-47bc-a081-fe2116060da0
ms.date: 12/05/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],GetStaticTerminals method, CMSPAddress.GetStaticTerminals, CMSPAddress::GetStaticTerminals, GetStaticTerminals, GetStaticTerminals method [TAPI 2.2], GetStaticTerminals method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_getstaticterminals, mspaddr/CMSPAddress::GetStaticTerminals, tapi3.cmspaddress_getstaticterminals
req.header: mspaddr.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CMSPAddress::GetStaticTerminals
 - mspaddr/CMSPAddress::GetStaticTerminals
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspaddr.h
api_name:
 - CMSPAddress.GetStaticTerminals
---

# CMSPAddress::GetStaticTerminals


## -description

The 
<b>GetStaticTerminals</b> method is called by our wrapper methods (
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals">get_StaticTerminals</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals">EnumerateStaticTerminals</a>) to get an array of static terminals that can be used on this address. This method updates the address' internal list of terminals by calling 
<a href="/windows/desktop/api/mspaddr/nf-mspaddr-cmspaddress-updateterminallist">UpdateTerminalList</a> if the list is not up to date. If the <i>ppTerminals</i> parameter is <b>NULL</b> or the *<i>pdwNumTerminals</i> parameter is not large enough to hold all the terminal pointers, this method simply returns (as *<i>pdwNumTerminals</i>) the number of terminals available. If <i>ppTerminals</i> is non-<b>NULL</b> and *<i>pdwNumTerminals</i> is large enough, it <b>AddRefs</b> each terminal pointer and places the array of terminal pointers in *<i>ppTerminals</i>, setting *<i>pdwNumTerminals</i> to the number of terminal pointers returned. If the derived MSP wants to change the set of terminals returned, it will probably override 
<a href="/windows/desktop/api/mspaddr/nf-mspaddr-cmspaddress-updateterminallist">UpdateTerminalList</a> rather than overriding this method.

## -parameters

### -param pdwNumTerminals [out]

Pointer to number of static terminals.

### -param ppTerminals [out]

Pointer to array of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interfaces.

## -see-also

<a href="/windows/desktop/api/mspaddr/nl-mspaddr-cmspaddress">CMSPAddress</a>