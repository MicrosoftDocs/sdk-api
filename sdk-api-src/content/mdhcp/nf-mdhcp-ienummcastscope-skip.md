---
UID: NF:mdhcp.IEnumMcastScope.Skip
title: IEnumMcastScope::Skip
author: windows-sdk-content
description: The Skip method skips over the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienummcastscope_skip.htm
old-project: Tapi
ms.assetid: 0e2255e7-586b-422f-a500-a32e6a460514
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IEnumMcastScope interface [TAPI 2.2],Skip method, IEnumMcastScope.Skip, IEnumMcastScope::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumMcastScope interface, _tapi3_ienummcastscope_skip, mdhcp/IEnumMcastScope::Skip, tapi3.ienummcastscope_skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mdhcp.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: MODEMSETTINGS, *PMODEMSETTINGS, *LPMODEMSETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mdhcp.dll
api_name:
-	IEnumMcastScope.Skip
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumMcastScope::Skip


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements to skip.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was not <i>celt</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/edc8be8e-635b-43f3-a4c1-7566e354cc3e">IEnumMcastScope</a>
 

 

