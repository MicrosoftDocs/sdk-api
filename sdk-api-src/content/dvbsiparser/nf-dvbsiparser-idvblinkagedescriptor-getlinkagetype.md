---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetLinkageType
title: IDvbLinkageDescriptor::GetLinkageType (dvbsiparser.h)
description: Gets a code that uniquely identifies the linkage type from a Digital Video Broadcast (DVB) linkage descriptor.helpviewer_keywords: ["GetLinkageType","GetLinkageType method [Microsoft TV Technologies]","GetLinkageType method [Microsoft TV Technologies]","IDvbLinkageDescriptor interface","IDvbLinkageDescriptor interface [Microsoft TV Technologies]","GetLinkageType method","IDvbLinkageDescriptor.GetLinkageType","IDvbLinkageDescriptor::GetLinkageType","dvbsiparser/IDvbLinkageDescriptor::GetLinkageType","mstv.idvblinkagedescriptor_getlinkagetype"]
old-location: mstv\idvblinkagedescriptor_getlinkagetype.htm
tech.root: mstv
ms.assetid: 54e17da4-df93-40a5-a359-274da77f585d
ms.date: 12/05/2018
ms.keywords: GetLinkageType, GetLinkageType method [Microsoft TV Technologies], GetLinkageType method [Microsoft TV Technologies],IDvbLinkageDescriptor interface, IDvbLinkageDescriptor interface [Microsoft TV Technologies],GetLinkageType method, IDvbLinkageDescriptor.GetLinkageType, IDvbLinkageDescriptor::GetLinkageType, dvbsiparser/IDvbLinkageDescriptor::GetLinkageType, mstv.idvblinkagedescriptor_getlinkagetype
f1_keywords:
- dvbsiparser/IDvbLinkageDescriptor.GetLinkageType
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
- IDvbLinkageDescriptor.GetLinkageType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbLinkageDescriptor::GetLinkageType


## -description


Gets a code that uniquely identifies the linkage type from a Digital Video Broadcast (DVB) linkage descriptor.


## -parameters




### -param pbVal [out]

Receives the linkage type code. For a list of linkage type codes, see Table 58 in Section 6.2.19 of the <i>DVB Specification for Service Information (SI) in DVB
systems
DVB (Document A038 Rev. 4)</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblinkagedescriptor">IDvbLinkageDescriptor</a>
 

 

