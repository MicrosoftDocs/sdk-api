---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetTextW
title: IIsdbDownloadContentDescriptor::GetTextW (dvbsiparser.h)
author: windows-sdk-content
description: Gets the text from an Integrated Services Digital Broadcasting (ISDB) download content descriptor that describes the descriptor contents, in Unicode text format.
old-location: mstv\iisdbdownloadcontentdescriptor_gettextw.htm
tech.root: mstv
ms.assetid: cf26ff9b-02d8-4470-bde5-6a18c62c6511
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTextW, GetTextW method [Microsoft TV Technologies], GetTextW method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetTextW method, IIsdbDownloadContentDescriptor.GetTextW, IIsdbDownloadContentDescriptor::GetTextW, dvbsiparser/IIsdbDownloadContentDescriptor::GetTextW, mstv.iisdbdownloadcontentdescriptor_gettextw
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
 - IIsdbDownloadContentDescriptor.GetTextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbDownloadContentDescriptor::GetTextW


## -description


 Gets the text from an Integrated Services Digital Broadcasting (ISDB) download content descriptor that describes the descriptor contents, in Unicode text format.


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrName [out]

Pointer to a buffer that receives the description text. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/beef626c-64b1-4f49-bb21-69022907004d">IIsdbDownloadContentDescriptor</a>
 

 

