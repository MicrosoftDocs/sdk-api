---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetCompatiblityDescriptor
title: IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor (dvbsiparser.h)

description: Gets data from the compatibility descriptor in an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The compatibility descriptor specifies a target to be updated by the download.
old-location: mstv\iisdbdownloadcontentdescriptor_getcompatiblitydescriptor.htm
tech.root: mstv
ms.assetid: 054fe987-49e1-4434-a9b9-6b1030fa2c41

ms.date: 12/05/2018
ms.keywords: GetCompatiblityDescriptor, GetCompatiblityDescriptor method [Microsoft TV Technologies], GetCompatiblityDescriptor method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetCompatiblityDescriptor method, IIsdbDownloadContentDescriptor.GetCompatiblityDescriptor, IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor, dvbsiparser/IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor, mstv.iisdbdownloadcontentdescriptor_getcompatiblitydescriptor
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IIsdbDownloadContentDescriptor.GetCompatiblityDescriptor"
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
 - IIsdbDownloadContentDescriptor.GetCompatiblityDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor


## -description


Gets data from the compatibility descriptor in  an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The compatibility descriptor specifies a target to be updated by the download.


## -parameters




### -param ppbData [out]

Pointer to a buffer that receives the compatibility descriptor. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>
 

 

