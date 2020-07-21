---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetTextW
title: IIsdbDataContentDescriptor::GetTextW (dvbsiparser.h)
description: Gets the text from an Integrated Services Digital Broadcasting (ISDB) data content descriptor that describes the contents of the descriptor, in Unicode text format.
helpviewer_keywords: ["GetTextW","GetTextW method [Microsoft TV Technologies]","GetTextW method [Microsoft TV Technologies]","IIsdbDataContentDescriptor interface","IIsdbDataContentDescriptor interface [Microsoft TV Technologies]","GetTextW method","IIsdbDataContentDescriptor.GetTextW","IIsdbDataContentDescriptor::GetTextW","dvbsiparser/IIsdbDataContentDescriptor::GetTextW","mstv.iisdbdatacontentdescriptor_gettextw"]
old-location: mstv\iisdbdatacontentdescriptor_gettextw.htm
tech.root: mstv
ms.assetid: b7abc2e2-4fb5-4b8b-8678-416056836aee
ms.date: 12/05/2018
ms.keywords: GetTextW, GetTextW method [Microsoft TV Technologies], GetTextW method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetTextW method, IIsdbDataContentDescriptor.GetTextW, IIsdbDataContentDescriptor::GetTextW, dvbsiparser/IIsdbDataContentDescriptor::GetTextW, mstv.iisdbdatacontentdescriptor_gettextw
f1_keywords:
- dvbsiparser/IIsdbDataContentDescriptor.GetTextW
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
- IIsdbDataContentDescriptor.GetTextW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDataContentDescriptor::GetTextW


## -description


 Gets the text from an Integrated Services Digital Broadcasting (ISDB) data content descriptor that describes the contents of the descriptor, in Unicode text format.


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrText [out]

Pointer to a buffer that receives the description text. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>
 

 

