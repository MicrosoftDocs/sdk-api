---
UID: NF:wuapi.IWindowsDriverUpdate2.CopyToCache
title: IWindowsDriverUpdate2::CopyToCache
author: windows-sdk-content
description: Copies the external update binaries to an update.
old-location: wua\iwindowsdriverupdate2_copytocache.htm
old-project: Wua_Sdk
ms.assetid: 3ad3f1bf-8da3-4d7d-8ed9-508422782861
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: CopyToCache, CopyToCache method [Windows Update Agent], CopyToCache method [Windows Update Agent],IWindowsDriverUpdate2 interface, IWindowsDriverUpdate2 interface [Windows Update Agent],CopyToCache method, IWindowsDriverUpdate2.CopyToCache, IWindowsDriverUpdate2::CopyToCache, wua.iwindowsdriverupdate2_copytocache, wuapi/IWindowsDriverUpdate2::CopyToCache
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IWindowsDriverUpdate2.CopyToCache
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IWindowsDriverUpdate2::CopyToCache


## -description


Copies the external update binaries  to an update.


## -parameters




### -param pFiles [in]

An <a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a> interface that contains the strings to be copied to an update.


#### - ignoreDigests [in]

If the value of the <i>ignoreDigests</i> parameter is <b>VARIANT_TRUE</b>, Windows Update Agent (WUA) ignores the digest mismatches when WUA copies from the location represented by the <i>pFiles</i> parameter.


If the value of <i>ignoreDigests</i> is <b>VARIANT_FALSE</b>, WUA does not ignore the digest mismatches when WUA copies from the location represented by the <i>pFiles</i> parameter.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer could not access the update site.

</td>
</tr>
</table>
 




## -remarks



This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is  implementing the interface has been locked down.




## -see-also




<a href="https://msdn.microsoft.com/9a2d6318-c5f0-41bc-a4df-bb9a53c9dee4">IWindowsDriverUpdate2</a>
 

 

