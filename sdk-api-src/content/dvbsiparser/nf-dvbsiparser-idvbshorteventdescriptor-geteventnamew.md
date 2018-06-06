---
UID: NF:dvbsiparser.IDvbShortEventDescriptor.GetEventNameW
title: IDvbShortEventDescriptor::GetEventNameW
author: windows-sdk-content
description: Gets the event name in Unicode string format from a Digital Video Broadcast (DVB) short event descriptor.
old-location: mstv\idvbshorteventdescriptor_geteventnamew.htm
old-project: mstv
ms.assetid: fbd14bf6-ba41-4f03-9f4f-74b6f16577c6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetEventNameW, GetEventNameW method [Microsoft TV Technologies], GetEventNameW method [Microsoft TV Technologies],IDvbShortEventDescriptor interface, IDvbShortEventDescriptor interface [Microsoft TV Technologies],GetEventNameW method, IDvbShortEventDescriptor.GetEventNameW, IDvbShortEventDescriptor::GetEventNameW, dvbsiparser/IDvbShortEventDescriptor::GetEventNameW, mstv.idvbshorteventdescriptor_geteventnamew
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
 - IDvbShortEventDescriptor.GetEventNameW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbShortEventDescriptor::GetEventNameW


## -description


Gets the event name in Unicode string format from a Digital Video Broadcast (DVB) short event descriptor.


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrName [out]

Pointer to a buffer that receives the event name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/039ae2e1-1dad-4a70-a054-bd95b0b500fb">IDvbShortEventDescriptor</a>
 

 

