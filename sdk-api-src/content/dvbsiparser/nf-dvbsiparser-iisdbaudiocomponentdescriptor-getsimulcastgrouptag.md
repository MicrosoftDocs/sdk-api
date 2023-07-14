---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetSimulcastGroupTag
title: IIsdbAudioComponentDescriptor::GetSimulcastGroupTag (dvbsiparser.h)
description: Gets the value of the simulcast_group_tag field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. For simulcast components, this field contains the tag that identifies all simulcast components.
helpviewer_keywords: ["GetSimulcastGroupTag","GetSimulcastGroupTag method [Microsoft TV Technologies]","GetSimulcastGroupTag method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetSimulcastGroupTag method","IIsdbAudioComponentDescriptor.GetSimulcastGroupTag","IIsdbAudioComponentDescriptor::GetSimulcastGroupTag","dvbsiparser/IIsdbAudioComponentDescriptor::GetSimulcastGroupTag","mstv.iisdbaudiocomponentdescriptor_getsimulcastgrouptag"]
old-location: mstv\iisdbaudiocomponentdescriptor_getsimulcastgrouptag.htm
tech.root: mstv
ms.assetid: 125fa9c2-eba0-497b-82ca-cc3223e40b44
ms.date: 12/05/2018
ms.keywords: GetSimulcastGroupTag, GetSimulcastGroupTag method [Microsoft TV Technologies], GetSimulcastGroupTag method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetSimulcastGroupTag method, IIsdbAudioComponentDescriptor.GetSimulcastGroupTag, IIsdbAudioComponentDescriptor::GetSimulcastGroupTag, dvbsiparser/IIsdbAudioComponentDescriptor::GetSimulcastGroupTag, mstv.iisdbaudiocomponentdescriptor_getsimulcastgrouptag
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
 - IIsdbAudioComponentDescriptor::GetSimulcastGroupTag
 - dvbsiparser/IIsdbAudioComponentDescriptor::GetSimulcastGroupTag
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
 - IIsdbAudioComponentDescriptor.GetSimulcastGroupTag
---

# IIsdbAudioComponentDescriptor::GetSimulcastGroupTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the value of the simulcast_group_tag field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. For simulcast components, this field contains the tag that identifies all simulcast components.

## -parameters

### -param pbVal [out]

Receives the simulcast group tag. For non-simulcast component, receives 0xFF.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>