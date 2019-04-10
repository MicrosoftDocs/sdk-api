---
UID: NF:adhoc.IEnumDot11AdHocInterfaces.Skip
title: IEnumDot11AdHocInterfaces::Skip (adhoc.h)
author: windows-sdk-content
description: Skips over the next specified number of elements in the enumeration sequence.
old-location: nwifi\ienumdot11adhocinterfaces_skip.htm
tech.root: NativeWiFi
ms.assetid: e5c61005-3de0-420e-a1ff-2c5f08bcc67f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumDot11AdHocInterfaces interface [NativeWIFI],Skip method, IEnumDot11AdHocInterfaces.Skip, IEnumDot11AdHocInterfaces::Skip, Skip, Skip method [NativeWIFI], Skip method [NativeWIFI],IEnumDot11AdHocInterfaces interface, adhoc/IEnumDot11AdHocInterfaces::Skip, nwifi.ienumdot11adhocinterfaces_skip
ms.topic: method
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
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
 - adhoc.h
api_name:
 - IEnumDot11AdHocInterfaces.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDot11AdHocInterfaces::Skip


## -description


Skips over the next specified number of elements in the enumeration sequence.


## -parameters




### -param cElt [in]

The number of elements to skip. 



## -returns



Possible return values include, but are not limited to, the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c61bbe3a-ad02-4182-bf10-1ed5fe307bd4">IEnumDot11AdHocInterfaces</a>
 

 

