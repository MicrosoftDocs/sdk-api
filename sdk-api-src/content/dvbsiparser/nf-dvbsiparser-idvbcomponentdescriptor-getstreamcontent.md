---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetStreamContent
title: IDvbComponentDescriptor::GetStreamContent (dvbsiparser.h)
description: Gets the stream content code for a Digital Video Broadcast (DVB) component descriptor.helpviewer_keywords: ["GetStreamContent","GetStreamContent method [Microsoft TV Technologies]","GetStreamContent method [Microsoft TV Technologies]","IDvbComponentDescriptor interface","IDvbComponentDescriptor interface [Microsoft TV Technologies]","GetStreamContent method","IDvbComponentDescriptor.GetStreamContent","IDvbComponentDescriptor::GetStreamContent","dvbsiparser/IDvbComponentDescriptor::GetStreamContent","mstv.idvbcomponentdescriptor_getstreamcontent"]
old-location: mstv\idvbcomponentdescriptor_getstreamcontent.htm
tech.root: mstv
ms.assetid: 3bfa86c4-2b94-43cd-842e-33cc03b713a5
ms.date: 12/05/2018
ms.keywords: GetStreamContent, GetStreamContent method [Microsoft TV Technologies], GetStreamContent method [Microsoft TV Technologies],IDvbComponentDescriptor interface, IDvbComponentDescriptor interface [Microsoft TV Technologies],GetStreamContent method, IDvbComponentDescriptor.GetStreamContent, IDvbComponentDescriptor::GetStreamContent, dvbsiparser/IDvbComponentDescriptor::GetStreamContent, mstv.idvbcomponentdescriptor_getstreamcontent
f1_keywords:
- dvbsiparser/IDvbComponentDescriptor.GetStreamContent
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
- IDvbComponentDescriptor.GetStreamContent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbComponentDescriptor::GetStreamContent


## -description


 Gets the stream content code for a Digital Video Broadcast (DVB) component descriptor.


## -parameters




### -param pbVal [out]

Receives the stream content code. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a list of content codes associated with the value returned in the <i>pbVal</i>  parameter, see Table 26 in Section 6.2.9 of the DVB standards document,  
      <a href="https://docs.microsoft.com/">Digital Video Broadcasting Specification for Service Information (SI) in DVB systems</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcomponentdescriptor">IDvbComponentDescriptor</a>
 

 

