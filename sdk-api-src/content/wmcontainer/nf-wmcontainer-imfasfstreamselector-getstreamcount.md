---
UID: NF:wmcontainer.IMFASFStreamSelector.GetStreamCount
title: IMFASFStreamSelector::GetStreamCount
author: windows-sdk-content
description: Retrieves the number of streams that are in the Advanced Systems Format (ASF) content.
old-location: mf\imfasfstreamselector_getstreamcount.htm
tech.root: medfound
ms.assetid: e1e80c32-bfd4-4404-9ccc-05b5077b83a6
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetStreamCount method, IMFASFStreamSelector.GetStreamCount, IMFASFStreamSelector::GetStreamCount, e1e80c32-bfd4-4404-9ccc-05b5077b83a6, mf.imfasfstreamselector_getstreamcount, wmcontainer/IMFASFStreamSelector::GetStreamCount
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
 - IMFASFStreamSelector.GetStreamCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFStreamSelector::GetStreamCount


## -description



Retrieves the number of streams that are in the Advanced Systems Format (ASF) content.




## -parameters




### -param pcStreams [out]

Receives the number of streams in the content.


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
 




## -see-also




<a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a>
 

 

