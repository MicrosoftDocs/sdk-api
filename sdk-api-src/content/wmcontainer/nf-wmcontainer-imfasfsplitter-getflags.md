---
UID: NF:wmcontainer.IMFASFSplitter.GetFlags
title: IMFASFSplitter::GetFlags
author: windows-sdk-content
description: Retrieves the option flags that are set on the ASF splitter.
old-location: mf\imfasfsplitter_getflags.htm
tech.root: medfound
ms.assetid: ba008e4a-98ad-4633-8b80-1d2ffce04b9c
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetFlags, GetFlags method [Media Foundation], GetFlags method [Media Foundation],IMFASFSplitter interface, IMFASFSplitter interface [Media Foundation],GetFlags method, IMFASFSplitter.GetFlags, IMFASFSplitter::GetFlags, ba008e4a-98ad-4633-8b80-1d2ffce04b9c, mf.imfasfsplitter_getflags, wmcontainer/IMFASFSplitter::GetFlags
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFSplitter.GetFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmcontainer.h
: 
- IMFASFSplitter.GetFlags
: 
---

# IMFASFSplitter::GetFlags


## -description



Retrieves the option flags that are set on the ASF splitter.




## -parameters




### -param pdwFlags [out]

Receives the option flags. This value is a bitwise <b>OR</b> of zero or more members of the <a href="https://msdn.microsoft.com/8eaad139-b487-4348-ae19-4251a2aeed14">MFASF_SPLITTERFLAGS</a> enumeration.


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
<i>pdwFlags</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/75d8b2a3-7c50-4dd5-8927-b11eb9f12602">IMFASFSplitter</a>



<a href="https://msdn.microsoft.com/5c70e5a0-7dd5-49c5-af35-4d9568871b41">IMFASFSplitter::SetFlags</a>
 

 

