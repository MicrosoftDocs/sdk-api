---
UID: NF:mfmp2dlna.IMFDLNASinkInit.Initialize
title: IMFDLNASinkInit::Initialize
author: windows-sdk-content
description: Initializes the Digital Living Network Alliance (DLNA) media sink.
old-location: mf\imfdlnasinkinit_initialize.htm
tech.root: medfound
ms.assetid: 48c3842c-7d88-4232-b882-363d9310ffe8
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMFDLNASinkInit interface [Media Foundation],Initialize method, IMFDLNASinkInit.Initialize, IMFDLNASinkInit::Initialize, Initialize, Initialize method [Media Foundation], Initialize method [Media Foundation],IMFDLNASinkInit interface, mf.imfdlnasinkinit_initialize, mfmp2dlna/IMFDLNASinkInit::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmp2dlna.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - mfmp2dlna.h
api_name:
 - IMFDLNASinkInit.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

