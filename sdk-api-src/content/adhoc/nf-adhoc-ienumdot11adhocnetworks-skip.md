---
UID: NF:adhoc.IEnumDot11AdHocNetworks.Skip
title: IEnumDot11AdHocNetworks::Skip
author: windows-sdk-content
description: Skips over the next specified number of elements in the enumeration sequence.
old-location: nwifi\ienumdot11adhocnetworks_skip.htm
old-project: NativeWiFi
ms.assetid: 31e182f8-6a19-4138-b799-7ad485868d19
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: IEnumDot11AdHocNetworks interface [NativeWIFI],Skip method, IEnumDot11AdHocNetworks.Skip, IEnumDot11AdHocNetworks::Skip, Skip, Skip method [NativeWIFI], Skip method [NativeWIFI],IEnumDot11AdHocNetworks interface, adhoc/IEnumDot11AdHocNetworks::Skip, nwifi.ienumdot11adhocnetworks_skip
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	adhoc.h
api_name:
-	IEnumDot11AdHocNetworks.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IEnumDot11AdHocNetworks::Skip


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




<a href="https://msdn.microsoft.com/5818e921-86bc-4f96-9ecd-3cb9c9a1a488">IEnumDot11AdHocNetworks</a>
 

 

