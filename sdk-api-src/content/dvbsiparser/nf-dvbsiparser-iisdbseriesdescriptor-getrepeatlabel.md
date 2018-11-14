---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetRepeatLabel
title: IIsdbSeriesDescriptor::GetRepeatLabel
author: windows-sdk-content
description: Gets a label that identifies a series repeat from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
old-location: mstv\iisdbseriesdescriptor_getrepeatlabel.htm
tech.root: MSTV
ms.assetid: 04b47836-0c27-41da-b71d-6c4abca6dd56
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRepeatLabel, GetRepeatLabel method [Microsoft TV Technologies], GetRepeatLabel method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetRepeatLabel method, IIsdbSeriesDescriptor.GetRepeatLabel, IIsdbSeriesDescriptor::GetRepeatLabel, dvbsiparser/IIsdbSeriesDescriptor::GetRepeatLabel, mstv.iisdbseriesdescriptor_getrepeatlabel
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
 - IIsdbSeriesDescriptor.GetRepeatLabel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IIsdbSeriesDescriptor.GetRepeatLabel
: 
---

# IIsdbSeriesDescriptor::GetRepeatLabel


## -description


Gets a label that identifies a series repeat from an Integrated Services Digital Broadcasting (ISDB) series descriptor.


## -parameters




### -param pbVal [out]

Receives the repeat label. If this label is zero, the series is an original broadcast.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07c4debc-1817-46ac-9f67-9b8637a04662">IIsdbSeriesDescriptor</a>
 

 

