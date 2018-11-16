---
UID: NF:strmif.IDvdInfo2.GetVMGAttributes
title: IDvdInfo2::GetVMGAttributes
author: windows-sdk-content
description: The GetVMGAttributes method retrieves attributes of all video, audio, and subpicture streams for the Video Manager Menu.
old-location: dshow\idvdinfo2_getvmgattributes.htm
tech.root: DirectShow
ms.assetid: ddb1059a-e1c5-4506-b565-fd871ad8385f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetVMGAttributes, GetVMGAttributes method [DirectShow], GetVMGAttributes method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetVMGAttributes method, IDvdInfo2.GetVMGAttributes, IDvdInfo2::GetVMGAttributes, IDvdInfo2GetVMGAttributes, dshow.idvdinfo2_getvmgattributes, strmif/IDvdInfo2::GetVMGAttributes
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
 - IDvdInfo2.GetVMGAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IDvdInfo2.GetVMGAttributes
: 
---

# IDvdInfo2::GetVMGAttributes


## -description



The <code>GetVMGAttributes</code> method retrieves attributes of all video, audio, and subpicture streams for the Video Manager Menu.




## -parameters




### -param pATR [out]

Pointer to a <a href="https://msdn.microsoft.com/074593e2-f4f4-44d3-a37c-209b4e798a52">DVD_MenuAttributes</a> structure that receives the attributes.


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



The Video Manager Menu is not associated with any particular title number.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

