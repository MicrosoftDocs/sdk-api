---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetTextW
title: IIsdbAudioComponentDescriptor::GetTextW (dvbsiparser.h)
description: Gets the component stream description from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor, in Unicode text format,.
helpviewer_keywords: ["GetTextW","GetTextW method [Microsoft TV Technologies]","GetTextW method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetTextW method","IIsdbAudioComponentDescriptor.GetTextW","IIsdbAudioComponentDescriptor::GetTextW","dvbsiparser/IIsdbAudioComponentDescriptor::GetTextW","mstv.iisdbaudiocomponentdescriptor_gettextw"]
old-location: mstv\iisdbaudiocomponentdescriptor_gettextw.htm
tech.root: mstv
ms.assetid: beeb31dd-28f8-45bb-bda0-0dbf6bca679b
ms.date: 12/05/2018
ms.keywords: GetTextW, GetTextW method [Microsoft TV Technologies], GetTextW method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetTextW method, IIsdbAudioComponentDescriptor.GetTextW, IIsdbAudioComponentDescriptor::GetTextW, dvbsiparser/IIsdbAudioComponentDescriptor::GetTextW, mstv.iisdbaudiocomponentdescriptor_gettextw
f1_keywords:
- dvbsiparser/IIsdbAudioComponentDescriptor.GetTextW
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IIsdbAudioComponentDescriptor.GetTextW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbAudioComponentDescriptor::GetTextW


## -description


Gets the component stream description from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor, in Unicode text format,. 


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrText [out]

Pointer to a buffer that receives the component stream description. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
 

 

