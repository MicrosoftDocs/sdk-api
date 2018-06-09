---
UID: NF:strmif.IDvdInfo2.GetDVDDirectory
title: IDvdInfo2::GetDVDDirectory
author: windows-sdk-content
description: The GetDVDDirectory method retrieves the root directory that is set in the DVD Navigator.
old-location: dshow\idvdinfo2_getdvddirectory.htm
old-project: DirectShow
ms.assetid: fad4dd0a-4831-4460-9631-ed06b6647f2d
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetDVDDirectory, GetDVDDirectory method [DirectShow], GetDVDDirectory method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDVDDirectory method, IDvdInfo2.GetDVDDirectory, IDvdInfo2::GetDVDDirectory, IDvdInfo2GetDVDDirectory, dshow.idvdinfo2_getdvddirectory, strmif/IDvdInfo2::GetDVDDirectory
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetDVDDirectory
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetDVDDirectory


## -description



The <code>GetDVDDirectory</code> method retrieves the root directory that is set in the DVD Navigator.




## -parameters




### -param pszwPath [out]

Pointer to a buffer that receives the path string.


### -param ulMaxSize [in]

Size of the buffer, in WCHARs.


### -param pulActualSize [out]

Pointer to a variable that receives the size of actual data returned, in WCHARs.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to hold the string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is not in a valid domain.

</td>
</tr>
</table>
 




## -remarks



This method is demonstrated in the DVDSample application in <b>CDvdCore::GetDriveLetter</b>.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

