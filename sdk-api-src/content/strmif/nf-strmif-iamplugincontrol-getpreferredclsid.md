---
UID: NF:strmif.IAMPluginControl.GetPreferredClsid
title: IAMPluginControl::GetPreferredClsid
author: windows-sdk-content
description: Searches the preferred list for a class identifier (CLSID) that matches a specified subtype.
old-location: dshow\iamplugincontrol_getpreferredclsid.htm
tech.root: DirectShow
ms.assetid: 69f55810-9a3a-48cd-8fd2-d091a906d229
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetPreferredClsid, GetPreferredClsid method [DirectShow], GetPreferredClsid method [DirectShow],IAMPluginControl interface, IAMPluginControl interface [DirectShow],GetPreferredClsid method, IAMPluginControl.GetPreferredClsid, IAMPluginControl::GetPreferredClsid, dshow.iamplugincontrol_getpreferredclsid, strmif/IAMPluginControl::GetPreferredClsid
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
 - IAMPluginControl.GetPreferredClsid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMPluginControl::GetPreferredClsid


## -description


Searches the preferred list for a class identifier (CLSID) that matches a specified subtype.




## -parameters




### -param subType [in]

A media subtype GUID to match.


### -param clsid [out]

Receives a CLSID from the preferred list.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
No CLSID matching this subtype was found.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/66720991-3a3f-4c45-a543-b8050d31fcc3">IAMPluginControl</a>



<a href="https://msdn.microsoft.com/938ba1b0-822e-4871-8786-b7eeee243867">Intelligent Connect</a>
 

 

