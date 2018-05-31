---
UID: NF:strmif.IDvdInfo.GetCurrentSubpictureAttributes
title: IDvdInfo::GetCurrentSubpictureAttributes
author: windows-sdk-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the attributes for the current subpicture stream in the current title or menu.
old-location: dshow\idvdinfo_getcurrentsubpictureattributes.htm
old-project: DirectShow
ms.assetid: 9beb31e3-b3ff-4c7a-922f-9f1e9725ddde
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetCurrentSubpictureAttributes, GetCurrentSubpictureAttributes method [DirectShow], GetCurrentSubpictureAttributes method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentSubpictureAttributes method, IDvdInfo.GetCurrentSubpictureAttributes, IDvdInfo::GetCurrentSubpictureAttributes, IDvdInfoGetCurrentSubpictureAttributes, dshow.idvdinfo_getcurrentsubpictureattributes, strmif/IDvdInfo::GetCurrentSubpictureAttributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IDvdInfo.GetCurrentSubpictureAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo::GetCurrentSubpictureAttributes


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the attributes for the current subpicture stream in the current title or menu.




## -parameters




### -param pATR [out]

Pointer to the retrieved subpicture attributes.


## -returns



Returns an <b>HRESULT</b> value .

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD is not initialized or domain is not DVD_DOMAIN_Title.

</td>
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
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>
 




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.

For information about DVD_SubpictureATR, see the DVD-Video specification.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b0c5dfe-aa1b-4ad0-9272-f1351e494b11">IDvdInfo Interface</a>
 

 

