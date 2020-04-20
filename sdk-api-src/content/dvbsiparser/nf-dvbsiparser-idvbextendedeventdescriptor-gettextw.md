---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetTextW
title: IDvbExtendedEventDescriptor::GetTextW (dvbsiparser.h)
description: Gets the text describing an itemfrom a Digital Video Broadcast (DVB) extended event descriptor, in string format.helpviewer_keywords: ["GetTextW","GetTextW method [Microsoft TV Technologies]","GetTextW method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetTextW method","IDvbExtendedEventDescriptor.GetTextW","IDvbExtendedEventDescriptor::GetTextW","dvbsiparser/IDvbExtendedEventDescriptor::GetTextW","mstv.idvbextendedeventdescriptor_gettextw"]
old-location: mstv\idvbextendedeventdescriptor_gettextw.htm
tech.root: mstv
ms.assetid: 18433c81-c58f-4657-90b0-183b1ad9f8e8
ms.date: 12/05/2018
ms.keywords: GetTextW, GetTextW method [Microsoft TV Technologies], GetTextW method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetTextW method, IDvbExtendedEventDescriptor.GetTextW, IDvbExtendedEventDescriptor::GetTextW, dvbsiparser/IDvbExtendedEventDescriptor::GetTextW, mstv.idvbextendedeventdescriptor_gettextw
f1_keywords:
- dvbsiparser/IDvbExtendedEventDescriptor.GetTextW
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
- IDvbExtendedEventDescriptor.GetTextW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbExtendedEventDescriptor::GetTextW


## -description


Gets the text describing an itemfrom a Digital Video Broadcast (DVB) extended event descriptor, in string format.


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrText [out]

Pointer to a buffer that receives the event description. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>
 

 

