---
UID: NF:mfmediaengine.IMFMediaTimeRange.AddRange
title: IMFMediaTimeRange::AddRange
author: windows-sdk-content
description: Adds a new range to the list of time ranges.
old-location: mf\imfmediatimerange_addrange.htm
tech.root: medfound
ms.assetid: 6BA36A44-78AC-4868-9E6A-601C0740E67A
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: AddRange, AddRange method [Media Foundation], AddRange method [Media Foundation],IMFMediaTimeRange interface, IMFMediaTimeRange interface [Media Foundation],AddRange method, IMFMediaTimeRange.AddRange, IMFMediaTimeRange::AddRange, mf.imfmediatimerange_addrange, mfmediaengine/IMFMediaTimeRange::AddRange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfmediaengine.h
api_name:
 - IMFMediaTimeRange.AddRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfmediaengine.h
: 
- IMFMediaTimeRange.AddRange
: 
---

# IMFMediaTimeRange::AddRange


## -description


Adds a new range to the list of time ranges.


## -parameters




### -param startTime [in]

The start time, in seconds.


### -param endTime [in]

The end time, in seconds.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the new range intersects a range already in the list, the two ranges are combined. Otherwise, the new range is added to the list.




## -see-also




<a href="https://msdn.microsoft.com/E39646E6-66F4-4413-A84B-43039689AEE7">IMFMediaTimeRange</a>
 

 

