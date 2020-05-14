---
UID: NF:dvbsiparser.IDvbDefaultAuthorityDescriptor.GetLength
title: IDvbDefaultAuthorityDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a default authority descriptor from a Digital Video Broadcast (DVB) content reference identifier (CRID).helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbDefaultAuthorityDescriptor interface","IDvbDefaultAuthorityDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbDefaultAuthorityDescriptor.GetLength","IDvbDefaultAuthorityDescriptor::GetLength","dvbsiparser/IDvbDefaultAuthorityDescriptor::GetLength","mstv.idvbdefaultauthoritydescriptor_getlength"]
old-location: mstv\idvbdefaultauthoritydescriptor_getlength.htm
tech.root: mstv
ms.assetid: 9eb76e79-d7a3-419b-9c3e-6d4e16486ff3
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbDefaultAuthorityDescriptor interface, IDvbDefaultAuthorityDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbDefaultAuthorityDescriptor.GetLength, IDvbDefaultAuthorityDescriptor::GetLength, dvbsiparser/IDvbDefaultAuthorityDescriptor::GetLength, mstv.idvbdefaultauthoritydescriptor_getlength
f1_keywords:
- dvbsiparser/IDvbDefaultAuthorityDescriptor.GetLength
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
- IDvbDefaultAuthorityDescriptor.GetLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbDefaultAuthorityDescriptor::GetLength


## -description


Gets the body length of a default authority descriptor from a Digital Video Broadcast (DVB) content reference identifier (CRID). 


## -parameters




### -param pbVal [out]

Receives the number of bytes in the descriptor.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdefaultauthoritydescriptor">IDvbDefaultAuthorityDescriptor</a>
 

 

