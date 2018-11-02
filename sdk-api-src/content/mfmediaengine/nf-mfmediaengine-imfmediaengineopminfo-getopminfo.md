---
UID: NF:mfmediaengine.IMFMediaEngineOPMInfo.GetOPMInfo
title: IMFMediaEngineOPMInfo::GetOPMInfo
author: windows-sdk-content
description: Gets status information about the Output Protection Manager (OPM).
old-location: mf\imfmediaengineopminfo_getopminfo.htm
tech.root: medfound
ms.assetid: 5e4a6e8f-5042-4de1-8cea-64b8e6cc928a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetOPMInfo, GetOPMInfo method [Media Foundation], GetOPMInfo method [Media Foundation],IMFMediaEngineOPMInfo interface, IMFMediaEngineOPMInfo interface [Media Foundation],GetOPMInfo method, IMFMediaEngineOPMInfo.GetOPMInfo, IMFMediaEngineOPMInfo::GetOPMInfo, mf.imfmediaengineopminfo_getopminfo, mfmediaengine/IMFMediaEngineOPMInfo::GetOPMInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFMediaEngineOPMInfo.GetOPMInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineOPMInfo::GetOPMInfo


## -description


Gets status information about the   <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>  (OPM).


## -parameters




### -param pStatus [out]

        A pointer to a <a href="https://msdn.microsoft.com/7C4D88F6-369B-4364-90C4-6D0F8DD1523B">MF_MEDIA_ENGINE_OPM_STATUS</a> enum type that indicates the OPM status.


### -param pConstricted [out]

A pointer to a <b>BOOL</b> type that indicates the constriction status.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
If any of the parameters are <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/399f81ac-38f8-4aaa-8b34-f5fd13b71402">IMFMediaEngineOPMInfo</a>
 

 

