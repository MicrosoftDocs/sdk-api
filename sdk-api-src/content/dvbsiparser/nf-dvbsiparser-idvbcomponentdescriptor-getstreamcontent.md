---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetStreamContent
title: IDvbComponentDescriptor::GetStreamContent (dvbsiparser.h)
description: Gets the stream content code for a Digital Video Broadcast (DVB) component descriptor.
helpviewer_keywords: ["GetStreamContent","GetStreamContent method [Microsoft TV Technologies]","GetStreamContent method [Microsoft TV Technologies]","IDvbComponentDescriptor interface","IDvbComponentDescriptor interface [Microsoft TV Technologies]","GetStreamContent method","IDvbComponentDescriptor.GetStreamContent","IDvbComponentDescriptor::GetStreamContent","dvbsiparser/IDvbComponentDescriptor::GetStreamContent","mstv.idvbcomponentdescriptor_getstreamcontent"]
old-location: mstv\idvbcomponentdescriptor_getstreamcontent.htm
tech.root: mstv
ms.assetid: 3bfa86c4-2b94-43cd-842e-33cc03b713a5
ms.date: 12/05/2018
ms.keywords: GetStreamContent, GetStreamContent method [Microsoft TV Technologies], GetStreamContent method [Microsoft TV Technologies],IDvbComponentDescriptor interface, IDvbComponentDescriptor interface [Microsoft TV Technologies],GetStreamContent method, IDvbComponentDescriptor.GetStreamContent, IDvbComponentDescriptor::GetStreamContent, dvbsiparser/IDvbComponentDescriptor::GetStreamContent, mstv.idvbcomponentdescriptor_getstreamcontent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbComponentDescriptor::GetStreamContent
 - dvbsiparser/IDvbComponentDescriptor::GetStreamContent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbComponentDescriptor.GetStreamContent
---

# IDvbComponentDescriptor::GetStreamContent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the stream content code for a Digital Video Broadcast (DVB) component descriptor.

## -parameters

### -param pbVal [out]

Receives the stream content code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For a list of content codes associated with the value returned in the <i>pbVal</i>  parameter, see Table 26 in Section 6.2.9 of the DVB standards document,  
      <a href="/">Digital Video Broadcasting Specification for Service Information (SI) in DVB systems</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcomponentdescriptor">IDvbComponentDescriptor</a>