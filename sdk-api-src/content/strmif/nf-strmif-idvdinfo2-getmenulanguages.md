---
UID: NF:strmif.IDvdInfo2.GetMenuLanguages
title: IDvdInfo2::GetMenuLanguages
author: windows-sdk-content
description: The GetMenuLanguages method retrieves all the languages available for all menus on the disc.
old-location: dshow\idvdinfo2_getmenulanguages.htm
tech.root: DirectShow
ms.assetid: 97c95208-e2fc-4c9a-b8ba-61419b96aec9
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetMenuLanguages, GetMenuLanguages method [DirectShow], GetMenuLanguages method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetMenuLanguages method, IDvdInfo2.GetMenuLanguages, IDvdInfo2::GetMenuLanguages, IDvdInfo2GetMenuLanguages, dshow.idvdinfo2_getmenulanguages, strmif/IDvdInfo2::GetMenuLanguages
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
 - IDvdInfo2.GetMenuLanguages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo2::GetMenuLanguages


## -description



The <code>GetMenuLanguages</code> method retrieves all the languages available for all menus on the disc.




## -parameters




### -param pLanguages [out]

Pointer to an <b>LCID</b> array that receives the languages returned. To retrieve only the number of languages available for menus, and not the actual languages themselves, specify <b>NULL</b> for <i>pLanguages</i>.


### -param ulMaxLanguages [in]

Maximum number of languages to retrieve.


### -param pulActualLanguages

TBD




#### - puActualLanguages [out]

Receives the actual number of languages retrieved.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is not initialized.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

