---
UID: NF:mfobjects.IMFPluginControl.IsDisabled
title: IMFPluginControl::IsDisabled (mfobjects.h)
description: Queries whether a class identifier (CLSID) appears in the blocked list. (IMFPluginControl.IsDisabled)
helpviewer_keywords: ["IMFPluginControl interface [Media Foundation]","IsDisabled method","IMFPluginControl.IsDisabled","IMFPluginControl::IsDisabled","IsDisabled","IsDisabled method [Media Foundation]","IsDisabled method [Media Foundation]","IMFPluginControl interface","mf.imfplugincontrol_imfplugincontrol__isdisabled","mfobjects/IMFPluginControl::IsDisabled"]
old-location: mf\imfplugincontrol_imfplugincontrol__isdisabled.htm
tech.root: mf
ms.assetid: 75f4f3a2-198d-41c0-b0fa-4a1fbefad7b6
ms.date: 12/05/2018
ms.keywords: IMFPluginControl interface [Media Foundation],IsDisabled method, IMFPluginControl.IsDisabled, IMFPluginControl::IsDisabled, IsDisabled, IsDisabled method [Media Foundation], IsDisabled method [Media Foundation],IMFPluginControl interface, mf.imfplugincontrol_imfplugincontrol__isdisabled, mfobjects/IMFPluginControl::IsDisabled
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPluginControl::IsDisabled
 - mfobjects/IMFPluginControl::IsDisabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFPluginControl.IsDisabled
---

# IMFPluginControl::IsDisabled


## -description

Queries whether a class identifier (CLSID) appears in the blocked list.

## -parameters

### -param pluginType [in]

Member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_type">MF_Plugin_Type</a> enumeration, specifying the type of object for the query.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>
