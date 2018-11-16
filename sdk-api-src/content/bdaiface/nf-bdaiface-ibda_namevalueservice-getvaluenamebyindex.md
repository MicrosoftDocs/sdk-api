---
UID: NF:bdaiface.IBDA_NameValueService.GetValueNameByIndex
title: IBDA_NameValueService::GetValueNameByIndex
author: windows-sdk-content
description: Gets a name, specified by index, from the device's list of name/value pairs.
old-location: mstv\ibda_namevalueservice_getvaluenamebyindex.htm
tech.root: mstv
ms.assetid: 4a860535-db03-4db7-912c-16b7e920151a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetValueNameByIndex, GetValueNameByIndex method [Microsoft TV Technologies], GetValueNameByIndex method [Microsoft TV Technologies],IBDA_NameValueService interface, IBDA_NameValueService interface [Microsoft TV Technologies],GetValueNameByIndex method, IBDA_NameValueService.GetValueNameByIndex, IBDA_NameValueService::GetValueNameByIndex, bdaiface/IBDA_NameValueService::GetValueNameByIndex, mstv.ibda_namevalueservice_getvaluenamebyindex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_NameValueService.GetValueNameByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdaiface.h
: 
- IBDA_NameValueService.GetValueNameByIndex
: 
---

# IBDA_NameValueService::GetValueNameByIndex


## -description


Gets a name, specified by index, from the device's list of name/value pairs.


## -parameters




### -param ulIndex [in]

The zero-based index of the name to get.


### -param pbstrName [out]

Receives the name as a <b>BSTR</b>. The caller must free the <b>BSTR</b> by calling <b>SysFreeString</b>.


## -returns



This method can return one of these values.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BDA_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>ulIndex</i> parameter is out of bounds.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693406(v=VS.85).aspx">IBDA_NameValueService</a>
 

 

