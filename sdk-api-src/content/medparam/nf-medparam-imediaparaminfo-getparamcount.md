---
UID: NF:medparam.IMediaParamInfo.GetParamCount
title: IMediaParamInfo::GetParamCount method
author: windows-driver-content
description: The GetParamCount method retrieves the number of parameters that the object supports.
old-location: dshow\imediaparaminfo_getparamcount.htm
old-project: DirectShow
ms.assetid: 0c518b8e-d5a7-40ba-9b10-4d23d4376890
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetParamCount method [DirectShow], GetParamCount method [DirectShow], IMediaParamInfo interface, GetParamCount,IMediaParamInfo.GetParamCount, IMediaParamInfo, IMediaParamInfo interface [DirectShow], GetParamCount method, IMediaParamInfo::GetParamCount, IMediaParamInfoGetParamCount, dshow.imediaparaminfo_getparamcount, medparam/IMediaParamInfo::GetParamCount
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IMediaParamInfo.GetParamCount
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaParamInfo::GetParamCount method


## -description



The <code>GetParamCount</code> method retrieves the number of parameters that the object supports.




## -parameters




### -param pdwParams [out]

Pointer to a variable that receives the number of parameters.


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
 

 

