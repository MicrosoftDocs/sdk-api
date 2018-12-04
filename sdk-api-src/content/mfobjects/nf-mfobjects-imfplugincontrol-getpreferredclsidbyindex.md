---
UID: NF:mfobjects.IMFPluginControl.GetPreferredClsidByIndex
title: IMFPluginControl::GetPreferredClsidByIndex
author: windows-sdk-content
description: Gets a class identifier (CLSID) from the preferred list, specified by index value.
old-location: mf\imfplugincontrol_imfplugincontrol__getpreferredclsidbyindex.htm
tech.root: medfound
ms.assetid: d99511ec-ac22-4166-b944-b0136ffcf01a
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: GetPreferredClsidByIndex, GetPreferredClsidByIndex method [Media Foundation], GetPreferredClsidByIndex method [Media Foundation],IMFPluginControl interface, IMFPluginControl interface [Media Foundation],GetPreferredClsidByIndex method, IMFPluginControl.GetPreferredClsidByIndex, IMFPluginControl::GetPreferredClsidByIndex, mf.imfplugincontrol_imfplugincontrol__getpreferredclsidbyindex, mfobjects/IMFPluginControl::GetPreferredClsidByIndex
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
 - IMFPluginControl.GetPreferredClsidByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPluginControl::GetPreferredClsidByIndex


## -description


Gets a class identifier (CLSID) from the preferred list, specified by index value.


## -parameters




### -param pluginType [in]

Member of the <a href="https://msdn.microsoft.com/f967cf3f-582c-457a-ba75-980feb2d9bf3">MF_Plugin_Type</a> enumeration, specifying the type of object to enumerate.


### -param index [in]

The zero-based index of the CLSID to retrieve.


### -param selector [out]

Receives the key name associated with the CLSID. The caller must free the memory for the returned string by calling the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function. For more information about the format of key names, see the Remarks section of <a href="https://msdn.microsoft.com/cdc6fd4f-c544-43bb-ba99-5468ef49949d">IMFPluginControl</a>.


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
 

 

