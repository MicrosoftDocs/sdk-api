---
UID: NF:dvbsiparser.IDvbDefaultAuthorityDescriptor.GetTag
title: IDvbDefaultAuthorityDescriptor::GetTag method
author: windows-driver-content
description: Gets the tag from the default authority descriptor for a Digital Video Broadcast (DVB) content reference identifier (CRID).
old-location: mstv\idvbdefaultauthoritydescriptor_gettag.htm
old-project: mstv
ms.assetid: d98d1a45-1d72-4142-8bb4-15ac4f738813
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies], IDvbDefaultAuthorityDescriptor interface, GetTag,IDvbDefaultAuthorityDescriptor.GetTag, IDvbDefaultAuthorityDescriptor, IDvbDefaultAuthorityDescriptor interface [Microsoft TV Technologies], GetTag method, IDvbDefaultAuthorityDescriptor::GetTag, dvbsiparser/IDvbDefaultAuthorityDescriptor::GetTag, mstv.idvbdefaultauthoritydescriptor_gettag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbDefaultAuthorityDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbDefaultAuthorityDescriptor::GetTag method


## -description


Gets the tag from the default authority descriptor for a Digital Video Broadcast (DVB) content reference identifier (CRID).


## -parameters




### -param pbVal [out]

Receives the content descriptor tag. For default authority descriptors, this tag value is "0x73". 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/42d10cb5-dea9-4fdb-a588-7bc647e0b95b">IDvbDefaultAuthorityDescriptor</a>
 

 

