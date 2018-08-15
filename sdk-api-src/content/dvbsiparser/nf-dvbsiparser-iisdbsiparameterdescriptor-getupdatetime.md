---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetUpdateTime
title: IIsdbSIParameterDescriptor::GetUpdateTime
author: windows-sdk-content
description: Gets the time at which a parameter becomes valid from a service information (SI) parameter descriptor.
old-location: mstv\iisdbsiparameterdescriptor_getupdatetime.htm
old-project: mstv
ms.assetid: 9cfe8387-4edf-453b-b41b-768496eae76c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetUpdateTime, GetUpdateTime method [Microsoft TV Technologies], GetUpdateTime method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetUpdateTime method, IIsdbSIParameterDescriptor.GetUpdateTime, IIsdbSIParameterDescriptor::GetUpdateTime, dvbsiparser/IIsdbSIParameterDescriptor::GetUpdateTime, mstv.iisdbsiparameterdescriptor_getupdatetime
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
 - IIsdbSIParameterDescriptor.GetUpdateTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSIParameterDescriptor::GetUpdateTime


## -description


 Gets the time at which a parameter becomes valid from a service information (SI) parameter descriptor. 


## -parameters




### -param pVal [out]

Receives the date/time value that indicates when the parameter becomes valid.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/264ae78d-cd72-49ff-b99b-2af637cc2917">IIsdbSIParameterDescriptor</a>
 

 

