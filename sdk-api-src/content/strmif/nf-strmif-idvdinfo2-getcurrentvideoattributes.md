---
UID: NF:strmif.IDvdInfo2.GetCurrentVideoAttributes
title: IDvdInfo2::GetCurrentVideoAttributes method
author: windows-driver-content
description: The GetCurrentVideoAttributes method retrieves the video attributes of the current title or menu.
old-location: dshow\idvdinfo2_getcurrentvideoattributes.htm
old-project: DirectShow
ms.assetid: 92bd3af9-7057-4bf7-9026-d4862c271a03
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetCurrentVideoAttributes method [DirectShow], GetCurrentVideoAttributes method [DirectShow], IDvdInfo2 interface, GetCurrentVideoAttributes,IDvdInfo2.GetCurrentVideoAttributes, IDvdInfo2, IDvdInfo2 interface [DirectShow], GetCurrentVideoAttributes method, IDvdInfo2::GetCurrentVideoAttributes, IDvdInfo2GetCurrentVideoAttributes, dshow.idvdinfo2_getcurrentvideoattributes, strmif/IDvdInfo2::GetCurrentVideoAttributes
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
-	IDvdInfo2.GetCurrentVideoAttributes
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetCurrentVideoAttributes method


## -description



The <code>GetCurrentVideoAttributes</code> method retrieves the video attributes of the current title or menu.




## -parameters




### -param pATR [out]

Pointer to a <a href="https://msdn.microsoft.com/b395a322-d63e-41a0-b97a-88f99aeba0e5">DVD_VideoAttributes</a> structure that receives the attributes.


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
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is not initialized.

</td>
</tr>
</table>
 




## -remarks



The use of this method is demonstrated in the DVDSample application in <b>CDvdCore::GetVideoAttributes()</b>.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

