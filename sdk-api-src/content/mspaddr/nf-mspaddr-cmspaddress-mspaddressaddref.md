---
UID: NF:mspaddr.CMSPAddress.MSPAddressAddRef
title: CMSPAddress::MSPAddressAddRef (mspaddr.h)
description: The MSPAddressAddRef method is the private AddRef method for the address.
helpviewer_keywords: ["CMSPAddress interface [TAPI 2.2]","MSPAddressAddRef method","CMSPAddress.MSPAddressAddRef","CMSPAddress::MSPAddressAddRef","MSPAddressAddRef","MSPAddressAddRef method [TAPI 2.2]","MSPAddressAddRef method [TAPI 2.2]","CMSPAddress interface","_tapi3_cmspaddress_mspaddressaddref","mspaddr/CMSPAddress::MSPAddressAddRef","tapi3.cmspaddress_mspaddressaddref"]
old-location: tapi3\cmspaddress_mspaddressaddref.htm
tech.root: tapi3
ms.assetid: 74a68851-f1c2-41ed-94cd-ec043be0f0d1
ms.date: 12/05/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],MSPAddressAddRef method, CMSPAddress.MSPAddressAddRef, CMSPAddress::MSPAddressAddRef, MSPAddressAddRef, MSPAddressAddRef method [TAPI 2.2], MSPAddressAddRef method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_mspaddressaddref, mspaddr/CMSPAddress::MSPAddressAddRef, tapi3.cmspaddress_mspaddressaddref
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
 - CMSPAddress::MSPAddressAddRef
 - mspaddr/CMSPAddress::MSPAddressAddRef
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
 - CMSPAddress.MSPAddressAddRef
---

# CMSPAddress::MSPAddressAddRef


## -description

The 
<b>MSPAddressAddRef</b> method is the private AddRef method for the address. MSP objects that keep references to the address must call this method instead of the normal COM AddRef method so that the reference is kept on the MSP address object instead of on the aggregate TAPI address object. This is crucial to ensure correct object lifetimes. A template helper function, <b>MSPAddRefHelper</b>, is provided to help the derived MSP implement this method. All the derived MSP has to do in its implementation of this method is call "MSPAddRefHelper(this)". This is needed simply to provide the type of the derived class to the template helper function.



## -see-also

<a href="/windows/desktop/api/mspaddr/nl-mspaddr-cmspaddress">CMSPAddress</a>
