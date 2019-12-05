---
UID: NF:dvbsiparser.IDvbShortEventDescriptor.GetEventNameW
title: IDvbShortEventDescriptor::GetEventNameW (dvbsiparser.h)
description: Gets the event name in Unicode string format from a Digital Video Broadcast (DVB) short event descriptor.
old-location: mstv\idvbshorteventdescriptor_geteventnamew.htm
tech.root: mstv
ms.assetid: fbd14bf6-ba41-4f03-9f4f-74b6f16577c6
ms.date: 12/05/2018
ms.keywords: GetEventNameW, GetEventNameW method [Microsoft TV Technologies], GetEventNameW method [Microsoft TV Technologies],IDvbShortEventDescriptor interface, IDvbShortEventDescriptor interface [Microsoft TV Technologies],GetEventNameW method, IDvbShortEventDescriptor.GetEventNameW, IDvbShortEventDescriptor::GetEventNameW, dvbsiparser/IDvbShortEventDescriptor::GetEventNameW, mstv.idvbshorteventdescriptor_geteventnamew
ms.topic: method
f1_keywords:
- dvbsiparser/IDvbShortEventDescriptor.GetEventNameW
dev_langs:
- c++
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
- IDvbShortEventDescriptor.GetEventNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbshorteventdescriptor">IDvbShortEventDescriptor</a>
 

 

