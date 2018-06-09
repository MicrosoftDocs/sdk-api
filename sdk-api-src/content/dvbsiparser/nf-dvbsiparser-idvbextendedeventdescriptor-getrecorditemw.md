---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetRecordItemW
title: IDvbExtendedEventDescriptor::GetRecordItemW
author: windows-sdk-content
description: Gets the item and descriptor from a Digital Videl Broadcast (DVB) extended event descriptor, in Unicode string format.
old-location: mstv\idvbextendedeventdescriptor_getrecorditemw.htm
old-project: mstv
ms.assetid: 39c046b0-d357-44c5-9abe-2fb3998b7677
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetRecordItemW, GetRecordItemW method [Microsoft TV Technologies], GetRecordItemW method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetRecordItemW method, IDvbExtendedEventDescriptor.GetRecordItemW, IDvbExtendedEventDescriptor::GetRecordItemW, dvbsiparser/IDvbExtendedEventDescriptor::GetRecordItemW, mstv.idvbextendedeventdescriptor_getrecorditemw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IDvbExtendedEventDescriptor.GetRecordItemW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbExtendedEventDescriptor::GetRecordItemW


## -description


Gets the item and descriptor from a  Digital Videl Broadcast (DVB) extended event descriptor, in Unicode string format.


## -parameters




### -param bRecordIndex [in]

Specifies the item record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/db065f1a-8354-4207-b7f7-d67adf094c70">IDvbExtendedEventDescriptor::GetCountOfRecords</a>
  method to get the number of records in the extended event descriptor.


### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrDesc [out]

Pointer to a buffer that receives the item description. The caller is responsible for freeing this memory.


### -param pbstrItem [out]

Pointer to a buffer that receives the item text. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/db100f17-f7b8-4252-8090-44567ab9dcbe">IDvbExtendedEventDescriptor</a>



<a href="https://msdn.microsoft.com/db065f1a-8354-4207-b7f7-d67adf094c70">IDvbExtendedEventDescriptor::GetCountOfRecords</a>
 

 

