---
UID: NF:strmif.IAMPluginControl.IsDisabled
title: IAMPluginControl::IsDisabled method
author: windows-driver-content
description: Queries whether a class identifier (CLSID) appears in the blocked list.
old-location: dshow\iamplugincontrol_isdisabled.htm
old-project: DirectShow
ms.assetid: 2d6bae28-7c26-47c4-8633-9ecc60293dc6
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAMPluginControl, IAMPluginControl interface [DirectShow], IsDisabled method, IAMPluginControl::IsDisabled, IsDisabled method [DirectShow], IsDisabled method [DirectShow], IAMPluginControl interface, IsDisabled,IAMPluginControl.IsDisabled, dshow.iamplugincontrol_isdisabled, strmif/IAMPluginControl::IsDisabled
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IAMPluginControl.IsDisabled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMPluginControl::IsDisabled method


## -description


Queries whether a class identifier (CLSID) appears in the blocked list.




## -parameters




### -param clsid [in]

The CLSID to search for.


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
The specified CLSID appears in the blocked list.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The specified CLSID is not in the blocked list.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/66720991-3a3f-4c45-a543-b8050d31fcc3">IAMPluginControl</a>



<a href="https://msdn.microsoft.com/938ba1b0-822e-4871-8786-b7eeee243867">Intelligent Connect</a>
 

 

