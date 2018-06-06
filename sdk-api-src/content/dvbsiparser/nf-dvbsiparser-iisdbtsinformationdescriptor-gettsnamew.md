---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetTSNameW
title: IIsdbTSInformationDescriptor::GetTSNameW
author: windows-sdk-content
description: Gets the transport stream name from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor, in Unicode string format.
old-location: mstv\iisdbtsinformationdescriptor_gettsnamew.htm
old-project: mstv
ms.assetid: 4c8900d1-1047-4b11-87e0-da1a72f511f7
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetTSNameW, GetTSNameW method [Microsoft TV Technologies], GetTSNameW method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetTSNameW method, IIsdbTSInformationDescriptor.GetTSNameW, IIsdbTSInformationDescriptor::GetTSNameW, dvbsiparser/IIsdbTSInformationDescriptor::GetTSNameW, mstv.iisdbtsinformationdescriptor_gettsnamew
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbTSInformationDescriptor.GetTSNameW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbTSInformationDescriptor::GetTSNameW


## -description


Gets the transport stream name  from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor, in Unicode string format.


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrName [out]

Pointer to a buffer that receives the transport stream name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3c8cd33c-5c2a-48a4-9e8a-f7dd03560848">IIsdbTSInformationDescriptor</a>
 

 

