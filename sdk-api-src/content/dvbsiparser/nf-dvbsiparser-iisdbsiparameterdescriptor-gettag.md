---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetTag
title: IIsdbSIParameterDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag that identifies a service information (SI) parameter descriptor.
old-location: mstv\iisdbsiparameterdescriptor_gettag.htm
old-project: mstv
ms.assetid: 9d38b158-39b0-4960-b392-086595680133
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbSIParameterDescriptor.GetTag, IIsdbSIParameterDescriptor::GetTag, dvbsiparser/IIsdbSIParameterDescriptor::GetTag, mstv.iisdbsiparameterdescriptor_gettag
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
 - IIsdbSIParameterDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSIParameterDescriptor::GetTag


## -description


Gets the tag that identifies a service information (SI) parameter descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For SI parameter descriptors, this value is 0xD7.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/264ae78d-cd72-49ff-b99b-2af637cc2917">IIsdbSIParameterDescriptor</a>
 

 

