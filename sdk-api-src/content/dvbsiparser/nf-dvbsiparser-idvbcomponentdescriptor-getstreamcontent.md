---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetStreamContent
title: IDvbComponentDescriptor::GetStreamContent
author: windows-driver-content
description: Gets the stream content code for a Digital Video Broadcast (DVB) component descriptor.
old-location: mstv\idvbcomponentdescriptor_getstreamcontent.htm
old-project: mstv
ms.assetid: 3bfa86c4-2b94-43cd-842e-33cc03b713a5
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetStreamContent, GetStreamContent method [Microsoft TV Technologies], GetStreamContent method [Microsoft TV Technologies],IDvbComponentDescriptor interface, IDvbComponentDescriptor interface [Microsoft TV Technologies],GetStreamContent method, IDvbComponentDescriptor.GetStreamContent, IDvbComponentDescriptor::GetStreamContent, dvbsiparser/IDvbComponentDescriptor::GetStreamContent, mstv.idvbcomponentdescriptor_getstreamcontent
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
-	IDvbComponentDescriptor.GetStreamContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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




<a href="https://msdn.microsoft.com/0dee15ee-5b36-4454-8092-6b57ef5063ce">IDvbComponentDescriptor</a>
 

 

