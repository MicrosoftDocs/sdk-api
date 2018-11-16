---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetTag
title: IIsdbTSInformationDescriptor::GetTag
author: windows-sdk-content
description: Receives the tag that identifies an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
old-location: mstv\iisdbtsinformationdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 77a7b225-2e7e-4fa2-a8f0-a5f18850cde6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbTSInformationDescriptor.GetTag, IIsdbTSInformationDescriptor::GetTag, dvbsiparser/IIsdbTSInformationDescriptor::GetTag, mstv.iisdbtsinformationdescriptor_gettag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IIsdbTSInformationDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IIsdbTSInformationDescriptor.GetTag
: 
---

# IIsdbTSInformationDescriptor::GetTag


## -description


Receives the tag that identifies an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For ISDB TS information descriptors, this value is 0xCD.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3c8cd33c-5c2a-48a4-9e8a-f7dd03560848">IIsdbTSInformationDescriptor</a>
 

 

