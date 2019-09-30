---
UID: NF:dvbsiparser.IIsdbEventGroupDescriptor.GetTag
title: IIsdbEventGroupDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) event group descriptor.
old-location: mstv\iisdbeventgroupdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 249c57a6-dcf8-4701-975d-39f8e8735798
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbEventGroupDescriptor interface, IIsdbEventGroupDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbEventGroupDescriptor.GetTag, IIsdbEventGroupDescriptor::GetTag, dvbsiparser/IIsdbEventGroupDescriptor::GetTag, mstv.iisdbeventgroupdescriptor_gettag
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IIsdbEventGroupDescriptor.GetTag"
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
 - IIsdbEventGroupDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbEventGroupDescriptor::GetTag


## -description


Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) event group descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For ISDB event group descriptors, this value is 0xD6.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbeventgroupdescriptor">IIsdbEventGroupDescriptor</a>
 

 

