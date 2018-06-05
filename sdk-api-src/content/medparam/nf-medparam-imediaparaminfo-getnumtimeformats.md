---
UID: NF:medparam.IMediaParamInfo.GetNumTimeFormats
title: IMediaParamInfo::GetNumTimeFormats
author: windows-sdk-content
description: The GetNumTimeFormats method retrieves the number of time formats that the object supports.
old-location: dshow\imediaparaminfo_getnumtimeformats.htm
old-project: DirectShow
ms.assetid: 5c398554-af2b-4e7d-8f5c-1c361535e7c6
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetNumTimeFormats, GetNumTimeFormats method [DirectShow], GetNumTimeFormats method [DirectShow],IMediaParamInfo interface, IMediaParamInfo interface [DirectShow],GetNumTimeFormats method, IMediaParamInfo.GetNumTimeFormats, IMediaParamInfo::GetNumTimeFormats, IMediaParamInfoGetNumTimeFormats, dshow.imediaparaminfo_getnumtimeformats, medparam/IMediaParamInfo::GetNumTimeFormats
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: medparam.h
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
req.typenames: MP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dmoguids.lib
-	Dmoguids.dll
api_name:
-	IMediaParamInfo.GetNumTimeFormats
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaParamInfo::GetNumTimeFormats


## -description



The <code>GetNumTimeFormats</code> method retrieves the number of time formats that the object supports.




## -parameters




### -param pdwNumTimeFormats [out]

Pointer to a variable that receives the number of supported time formats.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/80c7da71-7898-4bda-a181-09ad8906532a">IMediaParamInfo Interface</a>
 

 

