---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetSeriesNameW
title: IIsdbSeriesDescriptor::GetSeriesNameW
author: windows-sdk-content
description: Gets the series name from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
old-location: mstv\iisdbseriesdescriptor_getseriesnamew.htm
old-project: mstv
ms.assetid: 7638dc5b-6542-42f4-9996-f851704098a0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetSeriesNameW, GetSeriesNameW method [Microsoft TV Technologies], GetSeriesNameW method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetSeriesNameW method, IIsdbSeriesDescriptor.GetSeriesNameW, IIsdbSeriesDescriptor::GetSeriesNameW, dvbsiparser/IIsdbSeriesDescriptor::GetSeriesNameW, mstv.iisdbseriesdescriptor_getseriesnamew
ms.prod: windows
ms.technology: windows-sdk
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
-	IIsdbSeriesDescriptor.GetSeriesNameW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSeriesDescriptor::GetSeriesNameW


## -description


Gets the series name from an Integrated Services Digital Broadcasting (ISDB) series descriptor.


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrName [out]

Pointer to a buffer that receives the series name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07c4debc-1817-46ac-9f67-9b8637a04662">IIsdbSeriesDescriptor</a>
 

 

