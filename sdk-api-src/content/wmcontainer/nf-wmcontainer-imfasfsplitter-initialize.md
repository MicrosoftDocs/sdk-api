---
UID: NF:wmcontainer.IMFASFSplitter.Initialize
title: IMFASFSplitter::Initialize
author: windows-sdk-content
description: Resets the Advanced Systems Format (ASF) splitter and configures it to parse data from an ASF data section.
old-location: mf\imfasfsplitter_initialize.htm
old-project: medfound
ms.assetid: dd69c2f9-dabf-4bba-bb3b-75ec3208c189
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMFASFSplitter interface [Media Foundation],Initialize method, IMFASFSplitter.Initialize, IMFASFSplitter::Initialize, Initialize, Initialize method [Media Foundation], Initialize method [Media Foundation],IMFASFSplitter interface, dd69c2f9-dabf-4bba-bb3b-75ec3208c189, mf.imfasfsplitter_initialize, wmcontainer/IMFASFSplitter::Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFSplitter.Initialize
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFSplitter::Initialize


## -description



Resets the Advanced Systems Format (ASF) splitter and configures it to parse data from an ASF data section.




## -parameters




### -param pIContentInfo [in]

Pointer to the <a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a> interface of a ContentInfo object that describes the data to be parsed.


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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pIContentInfo</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/383b1cc6-4a77-4e0e-a766-6213c64b025c">ASF Splitter</a>



<a href="https://msdn.microsoft.com/75d8b2a3-7c50-4dd5-8927-b11eb9f12602">IMFASFSplitter</a>
 

 

