---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFDLNASinkInit::Initialize


## -description


Initializes the Digital Living Network Alliance (DLNA) media sink.


## -parameters




### -param pByteStream [in]

Pointer to a byte stream. The DLNA media sink writes data to this byte stream. The byte stream must be writable.


### -param fPal [in]

If <b>TRUE</b>, the DLNA media sink accepts PAL video formats. Otherwise, it accepts NTSC video  formats.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_ALREADY_INITIALIZED</b></b></dt>
</dl>
</td>
<td width="60%">
The method was already called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="https://msdn.microsoft.com/acda4e37-2dd0-4322-90fc-8f48d6842054">IMFMediaSink::Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fec2933a-aa1a-41e5-b697-fdae548b3789">IMFDLNASinkInit</a>
 

 

