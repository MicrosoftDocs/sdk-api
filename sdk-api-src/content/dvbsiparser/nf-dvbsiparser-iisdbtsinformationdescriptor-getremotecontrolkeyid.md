---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetRemoteControlKeyId
title: IIsdbTSInformationDescriptor::GetRemoteControlKeyId (dvbsiparser.h)
description: Gets the remote_control_key_id field value from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
helpviewer_keywords: ["GetRemoteControlKeyId","GetRemoteControlKeyId method [Microsoft TV Technologies]","GetRemoteControlKeyId method [Microsoft TV Technologies]","IIsdbTSInformationDescriptor interface","IIsdbTSInformationDescriptor interface [Microsoft TV Technologies]","GetRemoteControlKeyId method","IIsdbTSInformationDescriptor.GetRemoteControlKeyId","IIsdbTSInformationDescriptor::GetRemoteControlKeyId","dvbsiparser/IIsdbTSInformationDescriptor::GetRemoteControlKeyId","mstv.iisdbtsinformationdescriptor_getremotecontrolkeyid"]
old-location: mstv\iisdbtsinformationdescriptor_getremotecontrolkeyid.htm
tech.root: mstv
ms.assetid: 51162c5e-9ece-4c3d-9ab1-03d03a326efe
ms.date: 12/05/2018
ms.keywords: GetRemoteControlKeyId, GetRemoteControlKeyId method [Microsoft TV Technologies], GetRemoteControlKeyId method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetRemoteControlKeyId method, IIsdbTSInformationDescriptor.GetRemoteControlKeyId, IIsdbTSInformationDescriptor::GetRemoteControlKeyId, dvbsiparser/IIsdbTSInformationDescriptor::GetRemoteControlKeyId, mstv.iisdbtsinformationdescriptor_getremotecontrolkeyid
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IIsdbTSInformationDescriptor::GetRemoteControlKeyId
 - dvbsiparser/IIsdbTSInformationDescriptor::GetRemoteControlKeyId
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
 - IIsdbTSInformationDescriptor.GetRemoteControlKeyId
---

# IIsdbTSInformationDescriptor::GetRemoteControlKeyId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the remote_control_key_id field value from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor. This field indicates the recommended remote control key number to
which the applicable transport stream is assigned.

## -parameters

### -param pbVal [out]

Receives the remote_control_key_id field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbtsinformationdescriptor">IIsdbTSInformationDescriptor</a>