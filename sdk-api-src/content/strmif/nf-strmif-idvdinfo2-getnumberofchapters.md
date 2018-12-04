---
UID: NF:strmif.IDvdInfo2.GetNumberOfChapters
title: IDvdInfo2::GetNumberOfChapters
author: windows-sdk-content
description: The GetNumberOfChapters method retrieves the number of chapters in a given title.
old-location: dshow\idvdinfo2_getnumberofchapters.htm
tech.root: DirectShow
ms.assetid: 5899fa87-56e2-4287-9325-1d9eaedb892b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetNumberOfChapters, GetNumberOfChapters method [DirectShow], GetNumberOfChapters method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetNumberOfChapters method, IDvdInfo2.GetNumberOfChapters, IDvdInfo2::GetNumberOfChapters, IDvdInfo2GetNumberOfChapters, dshow.idvdinfo2_getnumberofchapters, strmif/IDvdInfo2::GetNumberOfChapters
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
 - IDvdInfo2.GetNumberOfChapters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo2::GetNumberOfChapters


## -description



The <code>GetNumberOfChapters</code> method retrieves the number of chapters in a given title.




## -parameters




### -param ulTitle [in]

Specifies the title.


### -param pulNumOfChapters [out]

Receives the number of chapters for the specified title.


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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is not initialized.

</td>
</tr>
</table>
 




## -remarks



Call this method to get the number of chapters before calling <a href="https://msdn.microsoft.com/b624aa7e-ff88-417c-8536-4ac38e8ae1ca">IDvdControl2::PlayChapter</a>, to ensure that you specify a valid chapter number.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

