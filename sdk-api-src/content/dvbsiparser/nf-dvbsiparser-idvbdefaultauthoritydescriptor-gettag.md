---
UID: NF:dvbsiparser.IDvbDefaultAuthorityDescriptor.GetTag
title: IDvbDefaultAuthorityDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag from the default authority descriptor for a Digital Video Broadcast (DVB) content reference identifier (CRID).
old-location: mstv\idvbdefaultauthoritydescriptor_gettag.htm
tech.root: mstv
ms.assetid: d98d1a45-1d72-4142-8bb4-15ac4f738813
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbDefaultAuthorityDescriptor interface, IDvbDefaultAuthorityDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbDefaultAuthorityDescriptor.GetTag, IDvbDefaultAuthorityDescriptor::GetTag, dvbsiparser/IDvbDefaultAuthorityDescriptor::GetTag, mstv.idvbdefaultauthoritydescriptor_gettag
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IDvbDefaultAuthorityDescriptor.GetTag"
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
 - IDvbDefaultAuthorityDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbDefaultAuthorityDescriptor::GetTag


## -description


Gets the tag from the default authority descriptor for a Digital Video Broadcast (DVB) content reference identifier (CRID).


## -parameters




### -param pbVal [out]

Receives the content descriptor tag. For default authority descriptors, this tag value is "0x73". 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdefaultauthoritydescriptor">IDvbDefaultAuthorityDescriptor</a>
 

 

