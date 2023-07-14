---
UID: NF:dvbsiparser.IPBDAEntitlementDescriptor.GetToken
title: IPBDAEntitlementDescriptor::GetToken (dvbsiparser.h)
description: Gets the entitlement token from the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetToken","GetToken method [Microsoft TV Technologies]","GetToken method [Microsoft TV Technologies]","IPBDAEntitlementDescriptor interface","IPBDAEntitlementDescriptor interface [Microsoft TV Technologies]","GetToken method","IPBDAEntitlementDescriptor.GetToken","IPBDAEntitlementDescriptor::GetToken","dvbsiparser/IPBDAEntitlementDescriptor::GetToken","mstv.ipbdaentitlementdescriptor_gettoken"]
old-location: mstv\ipbdaentitlementdescriptor_gettoken.htm
tech.root: mstv
ms.assetid: 3fc73b0c-cacb-491b-b25b-49eb57154a37
ms.date: 12/05/2018
ms.keywords: GetToken, GetToken method [Microsoft TV Technologies], GetToken method [Microsoft TV Technologies],IPBDAEntitlementDescriptor interface, IPBDAEntitlementDescriptor interface [Microsoft TV Technologies],GetToken method, IPBDAEntitlementDescriptor.GetToken, IPBDAEntitlementDescriptor::GetToken, dvbsiparser/IPBDAEntitlementDescriptor::GetToken, mstv.ipbdaentitlementdescriptor_gettoken
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
 - IPBDAEntitlementDescriptor::GetToken
 - dvbsiparser/IPBDAEntitlementDescriptor::GetToken
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
 - IPBDAEntitlementDescriptor.GetToken
---

# IPBDAEntitlementDescriptor::GetToken


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the entitlement token from the entitlement descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.

## -parameters

### -param ppbTokenBuffer [out]

Pointer to a buffer that receives the entitlement token. The caller must free this memory after use.

### -param pdwTokenLength [out]

Receives the entitlement token length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbdaentitlementdescriptor">IPBDAEntitlementDescriptor</a>