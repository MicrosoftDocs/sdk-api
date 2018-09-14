---
UID: NF:strmif.IDvdInfo2.GetCurrentDomain
title: IDvdInfo2::GetCurrentDomain
author: windows-sdk-content
description: The GetCurrentDomain method retrieves the domain in which the DVD Navigator is currently located.
old-location: dshow\idvdinfo2_getcurrentdomain.htm
tech.root: DirectShow
ms.assetid: ad850402-7b48-4517-a55f-42cfa75d3ee6
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetCurrentDomain, GetCurrentDomain method [DirectShow], GetCurrentDomain method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentDomain method, IDvdInfo2.GetCurrentDomain, IDvdInfo2::GetCurrentDomain, IDvdInfo2GetCurrentDomain, dshow.idvdinfo2_getcurrentdomain, strmif/IDvdInfo2::GetCurrentDomain
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetCurrentDomain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo2::GetCurrentDomain


## -description



The <code>GetCurrentDomain</code> method retrieves the domain in which the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is currently located.




## -parameters




### -param pDomain [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a> that receives the current domain.


## -returns



Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -remarks



You can use this method to test whether the DVD Navigator is finished playing in a particular title domain. An application doesn't have to test for the current domain before calling an <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> method such as <a href="https://msdn.microsoft.com/5cdea69e-7d32-470e-846b-1b2be5ca87b1">PlayTitle</a>, <a href="https://msdn.microsoft.com/bf57e2fd-c85f-430d-a1fa-5b59f7bfb8af">PlayForwards</a>, and so on. The DVD Navigator tests for the domain and simply does nothing, returning VFW_E_DVD_INVALIDDOMAIN, if the current command is invalid for the domain.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/4faa46d6-2ba2-44a3-b237-acac3b32f8b1">EC_DVD_DOMAIN_CHANGE</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

