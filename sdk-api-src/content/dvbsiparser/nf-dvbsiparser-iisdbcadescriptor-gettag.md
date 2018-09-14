---
UID: NF:dvbsiparser.IIsdbCADescriptor.GetTag
title: IIsdbCADescriptor::GetTag
author: windows-sdk-content
description: Gets the tag that identifies a conditional access (CA) descriptor.
old-location: mstv\iisdbcadescriptor_gettag.htm
tech.root: MSTV
ms.assetid: e8ed1538-3540-42c2-a465-ab6d580b0b31
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbCADescriptor interface, IIsdbCADescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbCADescriptor.GetTag, IIsdbCADescriptor::GetTag, dvbsiparser/IIsdbCADescriptor::GetTag, mstv.iisdbcadescriptor_gettag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbCADescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbCADescriptor::GetTag


## -description


Gets the tag that identifies a conditional access (CA) descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For conditional access descriptors, this value is 0x09.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6683f3db-636b-42bb-a46d-c175a4324023">IIsdbCADescriptor</a>
 

 

