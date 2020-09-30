---
UID: NF:mspaddr.CMSPAddress.ReceiveTSPAddressData
title: CMSPAddress::ReceiveTSPAddressData (mspaddr.h)
description: The ReceiveTSPAddressData method is called when a TSP data message is intended to be processed by the address rather than by a specific call. Your MSP must override this method if it wants to handle any per-address TSP messages.
helpviewer_keywords: ["CMSPAddress interface [TAPI 2.2]","ReceiveTSPAddressData method","CMSPAddress.ReceiveTSPAddressData","CMSPAddress::ReceiveTSPAddressData","ReceiveTSPAddressData","ReceiveTSPAddressData method [TAPI 2.2]","ReceiveTSPAddressData method [TAPI 2.2]","CMSPAddress interface","_tapi3_cmspaddress_receivetspaddressdata","mspaddr/CMSPAddress::ReceiveTSPAddressData","tapi3.cmspaddress_receivetspaddressdata"]
old-location: tapi3\cmspaddress_receivetspaddressdata.htm
tech.root: tapi3
ms.assetid: 56fc4024-bca0-405c-8a15-29ac8e486f80
ms.date: 12/05/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],ReceiveTSPAddressData method, CMSPAddress.ReceiveTSPAddressData, CMSPAddress::ReceiveTSPAddressData, ReceiveTSPAddressData, ReceiveTSPAddressData method [TAPI 2.2], ReceiveTSPAddressData method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_receivetspaddressdata, mspaddr/CMSPAddress::ReceiveTSPAddressData, tapi3.cmspaddress_receivetspaddressdata
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
 - CMSPAddress::ReceiveTSPAddressData
 - mspaddr/CMSPAddress::ReceiveTSPAddressData
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
 - CMSPAddress.ReceiveTSPAddressData
---

# CMSPAddress::ReceiveTSPAddressData


## -description

The 
<b>ReceiveTSPAddressData</b> method is called when a TSP data message is intended to be processed by the address rather than by a specific call. Your MSP must override this method if it wants to handle any per-address TSP messages.

## -parameters

### -param pBuffer [in, out]

Pointer to buffer.

### -param dwSize [out]

Pointer to number of characters in the buffer.

