---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetTag
title: IDvbComponentDescriptor::GetTag method
author: windows-driver-content
description: Gets the tag that identifies a Digital Video Broadcast (DVB) component descriptor.
old-location: mstv\idvbcomponentdescriptor_gettag.htm
old-project: mstv
ms.assetid: 680be3c5-ed02-4719-a510-cf84615f8738
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies], IDvbComponentDescriptor interface, GetTag,IDvbComponentDescriptor.GetTag, IDvbComponentDescriptor, IDvbComponentDescriptor interface [Microsoft TV Technologies], GetTag method, IDvbComponentDescriptor::GetTag, dvbsiparser/IDvbComponentDescriptor::GetTag, mstv.idvbcomponentdescriptor_gettag
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
-	IDvbComponentDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbComponentDescriptor::GetTag method


## -description


Gets the tag that identifies a Digital Video Broadcast (DVB) component  descriptor.


## -parameters




### -param pbVal [out]

Receives the identifier tag. For DVB component descriptors, this value is "0x50".


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0dee15ee-5b36-4454-8092-6b57ef5063ce">IDvbComponentDescriptor</a>
 

 

