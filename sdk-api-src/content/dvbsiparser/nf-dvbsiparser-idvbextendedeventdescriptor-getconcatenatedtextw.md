---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetConcatenatedTextW
title: IDvbExtendedEventDescriptor::GetConcatenatedTextW (dvbsiparser.h)

description: Gets the concatenation of the text description in the current item with the text description in the next item (both in Unicode format) of a Digital Video Broadcast (DVB) extended event descriptor.
old-location: mstv\idvbextendedeventdescriptor_getconcatenatedtextw.htm
tech.root: mstv
ms.assetid: d8cbfe2c-db33-449d-991c-5fb50d8d974f

ms.date: 12/05/2018
ms.keywords: GetConcatenatedTextW, GetConcatenatedTextW method [Microsoft TV Technologies], GetConcatenatedTextW method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetConcatenatedTextW method, IDvbExtendedEventDescriptor.GetConcatenatedTextW, IDvbExtendedEventDescriptor::GetConcatenatedTextW, dvbsiparser/IDvbExtendedEventDescriptor::GetConcatenatedTextW, mstv.idvbextendedeventdescriptor_getconcatenatedtextw
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IDvbExtendedEventDescriptor.GetConcatenatedTextW"
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
 - IDvbExtendedEventDescriptor.GetConcatenatedTextW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbExtendedEventDescriptor::GetConcatenatedTextW


## -description


Gets the concatenation of the text description in the current item with the text description in the next item (both in Unicode format) of a Digital Video Broadcast (DVB) extended event descriptor.


## -parameters




### -param FollowingDescriptor [in]

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a> interface for the next extended event descriptor that is associated with the current event descriptor.


### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrText [out]

Pointer to the buffer that receives the concatenated item text. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>
 

 

