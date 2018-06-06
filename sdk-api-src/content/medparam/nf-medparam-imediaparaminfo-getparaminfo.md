---
UID: NF:medparam.IMediaParamInfo.GetParamInfo
title: IMediaParamInfo::GetParamInfo
author: windows-sdk-content
description: The GetParamInfo method retrieves information about a specified parameter.
old-location: dshow\imediaparaminfo_getparaminfo.htm
old-project: DirectShow
ms.assetid: 80fdb9c2-d979-4671-981a-54d968b23042
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetParamInfo, GetParamInfo method [DirectShow], GetParamInfo method [DirectShow],IMediaParamInfo interface, IMediaParamInfo interface [DirectShow],GetParamInfo method, IMediaParamInfo.GetParamInfo, IMediaParamInfo::GetParamInfo, IMediaParamInfoGetParamInfo, dshow.imediaparaminfo_getparaminfo, medparam/IMediaParamInfo::GetParamInfo
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaParamInfo.GetParamInfo
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaParamInfo::GetParamInfo


## -description



The <code>GetParamInfo</code> method retrieves information about a specified parameter.




## -parameters




### -param dwParamIndex [in]

Zero-based index of the parameter.


### -param pInfo [out]

Pointer to an <a href="https://msdn.microsoft.com/91d2d08b-a55e-492f-a509-9c080cc438df">MP_PARAMINFO</a> structure that is filled with the parameter information.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
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
 




## -remarks



Call the <a href="https://msdn.microsoft.com/0c518b8e-d5a7-40ba-9b10-4d23d4376890">GetParamCount</a> method to retrieve the number of parameters that the object supports.




## -see-also




<a href="https://msdn.microsoft.com/80c7da71-7898-4bda-a181-09ad8906532a">IMediaParamInfo Interface</a>
 

 

