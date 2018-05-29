---
UID: NF:strmif.IDvdInfo2.GetDVDTextNumberOfLanguages
title: IDvdInfo2::GetDVDTextNumberOfLanguages
author: windows-sdk-content
description: The GetDVDTextNumberOfLanguages method retrieves the number of languages in which DVD text strings appear.
old-location: dshow\idvdinfo2_getdvdtextnumberoflanguages.htm
old-project: DirectShow
ms.assetid: 20c6ee1f-f20b-40c5-bc84-5ec1c07c0681
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetDVDTextNumberOfLanguages, GetDVDTextNumberOfLanguages method [DirectShow], GetDVDTextNumberOfLanguages method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDVDTextNumberOfLanguages method, IDvdInfo2.GetDVDTextNumberOfLanguages, IDvdInfo2::GetDVDTextNumberOfLanguages, IDvdInfo2GetDVDTextNumberOfLanguages, dshow.idvdinfo2_getdvdtextnumberoflanguages, strmif/IDvdInfo2::GetDVDTextNumberOfLanguages
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdInfo2.GetDVDTextNumberOfLanguages
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetDVDTextNumberOfLanguages


## -description



The <code>GetDVDTextNumberOfLanguages</code> method retrieves the number of languages in which DVD text strings appear.




## -parameters




### -param pulNumOfLangs [out]

Receives the number of text languages.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected internal error occurred.

</td>
</tr>
</table>
 




## -remarks



Depending on how the disc is authored, the number of languages will be valid either for the entire disc, or only for the current side of the disc.

If the DVD does not contain any text strings, the method succeeds, but <i>pulNumOfLangs</i> receives the value zero.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>



<a href="https://msdn.microsoft.com/6d415ebb-5cd0-4631-9404-f2ebabef2476">Working with DVD Text Strings</a>
 

 

