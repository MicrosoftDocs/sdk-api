---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetTag
title: IIsdbDataContentDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) data content descriptor.
old-location: mstv\iisdbdatacontentdescriptor_gettag.htm
tech.root: MSTV
ms.assetid: 308f44d6-0aae-418e-8aad-cc812c0cdb8a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbDataContentDescriptor.GetTag, IIsdbDataContentDescriptor::GetTag, dvbsiparser/IIsdbDataContentDescriptor::GetTag, mstv.iisdbdatacontentdescriptor_gettag
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
 - IIsdbDataContentDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbDataContentDescriptor::GetTag


## -description


Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) data content descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For ISDB data content descriptors, this value is 0xC7.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/91d55991-5994-4104-9a8f-01cfc347a96f">IIsdbDataContentDescriptor</a>
 

 

