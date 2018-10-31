---
UID: NF:mfobjects.IMFPluginControl.GetDisabledByIndex
title: IMFPluginControl::GetDisabledByIndex
author: windows-sdk-content
description: Gets a class identifier (CLSID) from the blocked list.
old-location: mf\imfplugincontrol_imfplugincontrol__getdisabledbyindex.htm
tech.root: medfound
ms.assetid: fae7ca09-3e37-444b-a4bc-bfd522917e3f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetDisabledByIndex, GetDisabledByIndex method [Media Foundation], GetDisabledByIndex method [Media Foundation],IMFPluginControl interface, IMFPluginControl interface [Media Foundation],GetDisabledByIndex method, IMFPluginControl.GetDisabledByIndex, IMFPluginControl::GetDisabledByIndex, mf.imfplugincontrol_imfplugincontrol__getdisabledbyindex, mfobjects/IMFPluginControl::GetDisabledByIndex
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMFPluginControl.GetDisabledByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPluginControl::GetDisabledByIndex


## -description


Gets a class identifier (CLSID) from the blocked list.


## -parameters




### -param pluginType [in]

Member of the <a href="https://msdn.microsoft.com/f967cf3f-582c-457a-ba75-980feb2d9bf3">MF_Plugin_Type</a> enumeration, specifying the type of object to enumerate.


### -param index [in]

The zero-based index of the CLSID to retrieve.


### -param clsid [out]

Receives the CLSID at the specified index.


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
The method succeeded.

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
<dt><b><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>index</i> parameter is out of range.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cdc6fd4f-c544-43bb-ba99-5468ef49949d">IMFPluginControl</a>
 

 

