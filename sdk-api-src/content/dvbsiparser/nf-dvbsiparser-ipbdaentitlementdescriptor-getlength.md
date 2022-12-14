---
UID: NF:dvbsiparser.IPBDAEntitlementDescriptor.GetLength
title: IPBDAEntitlementDescriptor::GetLength (dvbsiparser.h)
description: Gets the length of the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream, in bytes.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IPBDAEntitlementDescriptor interface","IPBDAEntitlementDescriptor interface [Microsoft TV Technologies]","GetLength method","IPBDAEntitlementDescriptor.GetLength","IPBDAEntitlementDescriptor::GetLength","dvbsiparser/IPBDAEntitlementDescriptor::GetLength","mstv.ipbdaentitlementdescriptor_getlength"]
old-location: mstv\ipbdaentitlementdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 51fc1ecc-ec18-415c-84f8-276ec581b24e
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IPBDAEntitlementDescriptor interface, IPBDAEntitlementDescriptor interface [Microsoft TV Technologies],GetLength method, IPBDAEntitlementDescriptor.GetLength, IPBDAEntitlementDescriptor::GetLength, dvbsiparser/IPBDAEntitlementDescriptor::GetLength, mstv.ipbdaentitlementdescriptor_getlength
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IPBDAEntitlementDescriptor::GetLength
 - dvbsiparser/IPBDAEntitlementDescriptor::GetLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDAEntitlementDescriptor.GetLength
---

# IPBDAEntitlementDescriptor::GetLength


## -description

Gets the length of the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream, in bytes.

## -parameters

### -param pwVal [out]

Receives the descriptor length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbdaentitlementdescriptor">IPBDAEntitlementDescriptor</a>