---
UID: NF:dvbsiparser.IDvbShortEventDescriptor.GetTextW
title: IDvbShortEventDescriptor::GetTextW
author: windows-sdk-content
description: Gets the text that describes the event in Unicode string format from a Digital Video Broadcast (DVB) short event descriptor.
old-location: mstv\idvbshorteventdescriptor_gettextw.htm
old-project: mstv
ms.assetid: 0770d24f-b421-4b00-809c-04fa53ca038c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTextW, GetTextW method [Microsoft TV Technologies], GetTextW method [Microsoft TV Technologies],IDvbShortEventDescriptor interface, IDvbShortEventDescriptor interface [Microsoft TV Technologies],GetTextW method, IDvbShortEventDescriptor.GetTextW, IDvbShortEventDescriptor::GetTextW, dvbsiparser/IDvbShortEventDescriptor::GetTextW, mstv.idvbshorteventdescriptor_gettextw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.redist: 
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbShortEventDescriptor.GetTextW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbShortEventDescriptor::GetTextW


## -description


Gets the text that describes the event in Unicode string format from a Digital Video Broadcast (DVB) short event descriptor.


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrText [out]

Pointer to a buffer that receives the event description text. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/039ae2e1-1dad-4a70-a054-bd95b0b500fb">IDvbShortEventDescriptor</a>
 

 

