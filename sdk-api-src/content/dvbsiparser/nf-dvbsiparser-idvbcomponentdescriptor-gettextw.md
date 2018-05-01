---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetTextW
title: IDvbComponentDescriptor::GetTextW method
author: windows-driver-content
description: Gets the text describing the elementary stream, in Unicode string format, from a Digital Video Broadcast (DVB) component descriptor.
old-location: mstv\idvbcomponentdescriptor_gettextw.htm
old-project: mstv
ms.assetid: 1b4ff757-24d0-4dca-8def-c8079724e571
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTextW method [Microsoft TV Technologies], GetTextW method [Microsoft TV Technologies], IDvbComponentDescriptor interface, GetTextW,IDvbComponentDescriptor.GetTextW, IDvbComponentDescriptor, IDvbComponentDescriptor interface [Microsoft TV Technologies], GetTextW method, IDvbComponentDescriptor::GetTextW, dvbsiparser/IDvbComponentDescriptor::GetTextW, mstv.idvbcomponentdescriptor_gettextw
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
-	IDvbComponentDescriptor.GetTextW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbComponentDescriptor::GetTextW method


## -description


Gets the text describing the elementary stream, in Unicode string format, from a Digital Video Broadcast (DVB) component descriptor.


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrText [out]

Receives the event description text. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0dee15ee-5b36-4454-8092-6b57ef5063ce">IDvbComponentDescriptor</a>
 

 

