---
UID: NF:imapi2.IDiscFormat2TrackAtOnceEventArgs.get_CurrentTrackNumber
title: IDiscFormat2TrackAtOnceEventArgs::get_CurrentTrackNumber
author: windows-sdk-content
description: Retrieves the current track number being written to the media.
old-location: imapi\idiscformat2trackatonceeventargs_get_currenttracknumber.htm
old-project: imapi
ms.assetid: e30afc06-b56b-49bc-8ad0-7446e16bdc95
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: IDiscFormat2TrackAtOnceEventArgs interface [IMAPI],get_CurrentTrackNumber method, IDiscFormat2TrackAtOnceEventArgs.get_CurrentTrackNumber, IDiscFormat2TrackAtOnceEventArgs::get_CurrentTrackNumber, get_CurrentTrackNumber, get_CurrentTrackNumber method [IMAPI], get_CurrentTrackNumber method [IMAPI],IDiscFormat2TrackAtOnceEventArgs interface, imapi.idiscformat2trackatonceeventargs_get_currenttracknumber, imapi2/IDiscFormat2TrackAtOnceEventArgs::get_CurrentTrackNumber
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2TrackAtOnceEventArgs.get_CurrentTrackNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2TrackAtOnceEventArgs::get_CurrentTrackNumber


## -description


Retrieves the current track number being written to the media.


## -parameters




### -param value [out]

Track number, ranging from 1 through 99.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/15d88768-f6e9-4d0a-a132-08f89fb3c34f">DDiscFormat2TrackAtOnceEvents</a>



<a href="https://msdn.microsoft.com/4bbcc3e1-0c85-4ed8-bbf6-e172e5896ed9">IDiscFormat2TrackAtOnceEventArgs</a>
 

 

