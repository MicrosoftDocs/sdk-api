---
UID: NF:dvbsiparser.IDvbLogicalChannelDescriptor.GetRecordLogicalChannelNumber
title: IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber
author: windows-sdk-content
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. .
old-location: mstv\idvblogicalchanneldescriptor_getrecordlogicalchannelnumber.htm
old-project: mstv
ms.assetid: fa74587a-ba11-449c-ba0d-bea371e7f019
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordLogicalChannelNumber, GetRecordLogicalChannelNumber method [DirectShow], GetRecordLogicalChannelNumber method [DirectShow],IDvbLogicalChannelDescriptor interface, IDvbLogicalChannelDescriptor interface [DirectShow],GetRecordLogicalChannelNumber method, IDvbLogicalChannelDescriptor.GetRecordLogicalChannelNumber, IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber, IDvbLogicalChannelDescriptorGetRecordLogicalChannelNumber, dvbsiparser/IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber, mstv.idvblogicalchanneldescriptor_getrecordlogicalchannelnumber
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
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
 - IDvbLogicalChannelDescriptor.GetRecordLogicalChannelNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.</div>
<div> </div>




The <b>GetRecordLogicalChannelNumber</b> method returns the logical channel number at a specified index in the channel list.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the logical channel number to return. To get the number of logical channel numbers in the descriptor, call <a href="https://msdn.microsoft.com/97cadf6c-2549-4a7f-9ecb-c16298769a21">IDvbLogicalChannelDescriptor::GetCountOfRecords</a>.
          


### -param pwVal [out]

Receives the logical_channel_number field.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6e0a99e9-088f-420c-bb60-2d324aa28227">IDvbLogicalChannelDescriptor</a>
 

 

