---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetTag
title: IDvbComponentDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag that identifies a Digital Video Broadcast (DVB) component descriptor.
old-location: mstv\idvbcomponentdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 680be3c5-ed02-4719-a510-cf84615f8738
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbComponentDescriptor interface, IDvbComponentDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbComponentDescriptor.GetTag, IDvbComponentDescriptor::GetTag, dvbsiparser/IDvbComponentDescriptor::GetTag, mstv.idvbcomponentdescriptor_gettag
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
 - IDvbComponentDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbComponentDescriptor::GetTag


## -description


Gets the tag that identifies a Digital Video Broadcast (DVB) component  descriptor.


## -parameters




### -param pbVal [out]

Receives the identifier tag. For DVB component descriptors, this value is "0x50".


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcomponentdescriptor">IDvbComponentDescriptor</a>
 

 

