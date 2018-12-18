---
UID: NF:mfobjects.IMFPluginControl.IsDisabled
title: IMFPluginControl::IsDisabled
author: windows-sdk-content
description: Queries whether a class identifier (CLSID) appears in the blocked list.
old-location: mf\imfplugincontrol_imfplugincontrol__isdisabled.htm
tech.root: medfound
ms.assetid: 75f4f3a2-198d-41c0-b0fa-4a1fbefad7b6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFPluginControl interface [Media Foundation],IsDisabled method, IMFPluginControl.IsDisabled, IMFPluginControl::IsDisabled, IsDisabled, IsDisabled method [Media Foundation], IsDisabled method [Media Foundation],IMFPluginControl interface, mf.imfplugincontrol_imfplugincontrol__isdisabled, mfobjects/IMFPluginControl::IsDisabled
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - mfobjects.h
api_name:
 - IMFPluginControl.IsDisabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPluginControl::IsDisabled


## -description


Queries whether a class identifier (CLSID) appears in the blocked list.


## -parameters




### -param pluginType [in]

Member of the <a href="https://msdn.microsoft.com/f967cf3f-582c-457a-ba75-980feb2d9bf3">MF_Plugin_Type</a> enumeration, specifying the type of object for the query.


### -param clsid [in]

The CLSID to search for.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The specified CLSID appears in the blocked list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></b></dt>
</dl>
</td>
<td width="60%">
The specified CLSID is not in the blocked list.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cdc6fd4f-c544-43bb-ba99-5468ef49949d">IMFPluginControl</a>
 

 

