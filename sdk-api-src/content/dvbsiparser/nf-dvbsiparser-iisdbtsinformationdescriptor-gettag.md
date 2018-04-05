---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetTag
title: IIsdbTSInformationDescriptor::GetTag method
author: windows-driver-content
description: Receives the tag that identifies an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
old-location: mstv\iisdbtsinformationdescriptor_gettag.htm
old-project: mstv
ms.assetid: 77a7b225-2e7e-4fa2-a8f0-a5f18850cde6
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies], IIsdbTSInformationDescriptor interface, GetTag,IIsdbTSInformationDescriptor.GetTag, IIsdbTSInformationDescriptor, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies], GetTag method, IIsdbTSInformationDescriptor::GetTag, dvbsiparser/IIsdbTSInformationDescriptor::GetTag, mstv.iisdbtsinformationdescriptor_gettag
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbTSInformationDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbTSInformationDescriptor::GetTag method


## -description


Receives the tag that identifies an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For ISDB TS information descriptors, this value is 0xCD.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3c8cd33c-5c2a-48a4-9e8a-f7dd03560848">IIsdbTSInformationDescriptor</a>
 

 

