---
UID: NF:wmsdkidl.WMCreateProfileManager
title: WMCreateProfileManager function (wmsdkidl.h)
author: windows-sdk-content
description: The WMCreateProfileManager function creates a profile manager object.
old-location: wmformat\wmcreateprofilemanager.htm
tech.root: wmformat
ms.assetid: 77eea431-74a0-449e-847e-7885ab33bda1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMCreateProfileManager, WMCreateProfileManager function [windows Media Format], wmformat.wmcreateprofilemanager, wmsdkidl/WMCreateProfileManager
ms.topic: function
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateProfileManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCreateProfileManager function


## -description



The <b>WMCreateProfileManager</b> function creates a profile manager object.




## -parameters




### -param ppProfileManager [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd757385(v=VS.85).aspx">IWMProfileManager</a> interface of the newly created profile manager object.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -remarks



When a profile manager object is created, it parses all of the system profiles. Creating and releasing a profile manager every time you need to use it will adversely affect performance. You should create a profile manager once in your application and release it only when you no longer need to use it.




## -see-also




<a href="https://msdn.microsoft.com/10fa8f96-8030-4727-af5d-7c06229d05d8">Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757228(v=VS.85).aspx">IWMMediaProps Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757385(v=VS.85).aspx">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>
 

 

