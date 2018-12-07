---
UID: NF:strmif.IAMPluginControl.GetDisabledByIndex
title: IAMPluginControl::GetDisabledByIndex
author: windows-sdk-content
description: Gets a class identifier (CLSID) from the blocked list.
old-location: dshow\iamplugincontrol_getdisabledbyindex.htm
tech.root: DirectShow
ms.assetid: 7c55e37b-46f1-4283-bea4-3884ae730906
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDisabledByIndex, GetDisabledByIndex method [DirectShow], GetDisabledByIndex method [DirectShow],IAMPluginControl interface, IAMPluginControl interface [DirectShow],GetDisabledByIndex method, IAMPluginControl.GetDisabledByIndex, IAMPluginControl::GetDisabledByIndex, dshow.iamplugincontrol_getdisabledbyindex, strmif/IAMPluginControl::GetDisabledByIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Strmif.h
api_name:
 - IAMPluginControl.GetDisabledByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMPluginControl::GetDisabledByIndex


## -description


Gets a class identifier (CLSID) from the blocked list.




## -parameters




### -param index [in]

The zero-based index of the CLSID to retrieve.




### -param clsid [out]

Receives the CLSID at the specified index.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
The <i>index</i> parameter is out of range.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/66720991-3a3f-4c45-a543-b8050d31fcc3">IAMPluginControl</a>



<a href="https://msdn.microsoft.com/938ba1b0-822e-4871-8786-b7eeee243867">Intelligent Connect</a>
 

 

