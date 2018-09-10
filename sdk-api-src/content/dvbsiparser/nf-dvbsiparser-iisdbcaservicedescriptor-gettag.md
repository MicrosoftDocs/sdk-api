---
UID: NF:dvbsiparser.IIsdbCAServiceDescriptor.GetTag
title: IIsdbCAServiceDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag that identifies a conditional access (CA) service descriptor.
old-location: mstv\iisdbcaservicedescriptor_gettag.htm
tech.root: mstv
ms.assetid: 55f7b955-03f6-4c40-bd73-175bf3453ed0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbCAServiceDescriptor interface, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbCAServiceDescriptor.GetTag, IIsdbCAServiceDescriptor::GetTag, dvbsiparser/IIsdbCAServiceDescriptor::GetTag, mstv.iisdbcaservicedescriptor_gettag
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
 - IIsdbCAServiceDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbCAServiceDescriptor::GetTag


## -description


Gets the tag that identifies a conditional access (CA) service descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For conditional access service descriptors, this value is 0xCC.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6d56e39d-3c7a-4c55-8d07-00e25eba18bd">IIsdbCAServiceDescriptor</a>
 

 

