---
UID: NF:dvbsiparser.IIsdbCAServiceDescriptor.GetCABroadcasterGroupId
title: IIsdbCAServiceDescriptor::GetCABroadcasterGroupId (dvbsiparser.h)
description: Gets the conditional access (CA) broadcaster group identifier from a CA service descriptor.
helpviewer_keywords: ["GetCABroadcasterGroupId","GetCABroadcasterGroupId method [Microsoft TV Technologies]","GetCABroadcasterGroupId method [Microsoft TV Technologies]","IIsdbCAServiceDescriptor interface","IIsdbCAServiceDescriptor interface [Microsoft TV Technologies]","GetCABroadcasterGroupId method","IIsdbCAServiceDescriptor.GetCABroadcasterGroupId","IIsdbCAServiceDescriptor::GetCABroadcasterGroupId","dvbsiparser/IIsdbCAServiceDescriptor::GetCABroadcasterGroupId","mstv.iisdbcaservicedescriptor_getcabroadcastergroupid"]
old-location: mstv\iisdbcaservicedescriptor_getcabroadcastergroupid.htm
tech.root: mstv
ms.assetid: cc783e34-3544-4bcf-9e76-cb098c89cd65
ms.date: 12/05/2018
ms.keywords: GetCABroadcasterGroupId, GetCABroadcasterGroupId method [Microsoft TV Technologies], GetCABroadcasterGroupId method [Microsoft TV Technologies],IIsdbCAServiceDescriptor interface, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],GetCABroadcasterGroupId method, IIsdbCAServiceDescriptor.GetCABroadcasterGroupId, IIsdbCAServiceDescriptor::GetCABroadcasterGroupId, dvbsiparser/IIsdbCAServiceDescriptor::GetCABroadcasterGroupId, mstv.iisdbcaservicedescriptor_getcabroadcastergroupid
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
 - IIsdbCAServiceDescriptor::GetCABroadcasterGroupId
 - dvbsiparser/IIsdbCAServiceDescriptor::GetCABroadcasterGroupId
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
 - IIsdbCAServiceDescriptor.GetCABroadcasterGroupId
---

# IIsdbCAServiceDescriptor::GetCABroadcasterGroupId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the conditional access (CA) broadcaster group identifier from a CA service descriptor.

## -parameters

### -param pbVal [out]

Receives the conditional access broadcaster group identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcaservicedescriptor">IIsdbCAServiceDescriptor</a>