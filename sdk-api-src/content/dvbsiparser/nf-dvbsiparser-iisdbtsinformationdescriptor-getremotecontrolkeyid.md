---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetRemoteControlKeyId
title: IIsdbTSInformationDescriptor::GetRemoteControlKeyId (dvbsiparser.h)

description: Gets the remote_control_key_id field value from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
old-location: mstv\iisdbtsinformationdescriptor_getremotecontrolkeyid.htm
tech.root: mstv
ms.assetid: 51162c5e-9ece-4c3d-9ab1-03d03a326efe

ms.date: 12/05/2018
ms.keywords: GetRemoteControlKeyId, GetRemoteControlKeyId method [Microsoft TV Technologies], GetRemoteControlKeyId method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetRemoteControlKeyId method, IIsdbTSInformationDescriptor.GetRemoteControlKeyId, IIsdbTSInformationDescriptor::GetRemoteControlKeyId, dvbsiparser/IIsdbTSInformationDescriptor::GetRemoteControlKeyId, mstv.iisdbtsinformationdescriptor_getremotecontrolkeyid
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IIsdbTSInformationDescriptor.GetRemoteControlKeyId"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbTSInformationDescriptor.GetRemoteControlKeyId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbTSInformationDescriptor::GetRemoteControlKeyId


## -description


Gets the remote_control_key_id field value from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor. This field indicates the recommended remote control key number to
which the applicable transport stream is assigned.


## -parameters




### -param pbVal [out]

Receives the remote_control_key_id field value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbtsinformationdescriptor">IIsdbTSInformationDescriptor</a>
 

 

