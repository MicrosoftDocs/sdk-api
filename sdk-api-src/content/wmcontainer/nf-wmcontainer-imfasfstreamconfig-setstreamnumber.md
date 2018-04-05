---
UID: NF:wmcontainer.IMFASFStreamConfig.SetStreamNumber
title: IMFASFStreamConfig::SetStreamNumber method
author: windows-driver-content
description: Assigns a stream number to the stream.
old-location: mf\imfasfstreamconfig_setstreamnumber.htm
old-project: medfound
ms.assetid: 5b22d857-fced-4094-a0ad-891f3ccf8b18
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: 5b22d857-fced-4094-a0ad-891f3ccf8b18, IMFASFStreamConfig, IMFASFStreamConfig interface [Media Foundation], SetStreamNumber method, IMFASFStreamConfig::SetStreamNumber, SetStreamNumber method [Media Foundation], SetStreamNumber method [Media Foundation], IMFASFStreamConfig interface, SetStreamNumber,IMFASFStreamConfig.SetStreamNumber, mf.imfasfstreamconfig_setstreamnumber, wmcontainer/IMFASFStreamConfig::SetStreamNumber
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFASFStreamConfig.SetStreamNumber
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFStreamConfig::SetStreamNumber method


## -description



Assigns a stream number to the stream.




## -parameters




### -param wStreamNum [in]

The number to assign to the stream.


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
</table>
 




## -remarks



Stream numbers start from 1 and do not need to be sequential.




## -see-also




<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>
 

 

