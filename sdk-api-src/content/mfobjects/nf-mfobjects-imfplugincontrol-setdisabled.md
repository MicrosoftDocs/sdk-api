---
UID: NF:mfobjects.IMFPluginControl.SetDisabled
title: IMFPluginControl::SetDisabled (mfobjects.h)
description: Adds a class identifier (CLSID) to the blocked list, or removes a CLSID from the list. (IMFPluginControl.SetDisabled)
helpviewer_keywords: ["IMFPluginControl interface [Media Foundation]","SetDisabled method","IMFPluginControl.SetDisabled","IMFPluginControl::SetDisabled","SetDisabled","SetDisabled method [Media Foundation]","SetDisabled method [Media Foundation]","IMFPluginControl interface","mf.imfplugincontrol_imfplugincontrol__setdisabled","mfobjects/IMFPluginControl::SetDisabled"]
old-location: mf\imfplugincontrol_imfplugincontrol__setdisabled.htm
tech.root: mf
ms.assetid: ff50e746-42f5-4fbe-a904-f83b3c691d32
ms.date: 12/05/2018
ms.keywords: IMFPluginControl interface [Media Foundation],SetDisabled method, IMFPluginControl.SetDisabled, IMFPluginControl::SetDisabled, SetDisabled, SetDisabled method [Media Foundation], SetDisabled method [Media Foundation],IMFPluginControl interface, mf.imfplugincontrol_imfplugincontrol__setdisabled, mfobjects/IMFPluginControl::SetDisabled
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
 - IMFPluginControl::SetDisabled
 - mfobjects/IMFPluginControl::SetDisabled
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
 - IMFPluginControl.SetDisabled
---

# IMFPluginControl::SetDisabled


## -description

Adds a class identifier (CLSID) to the blocked list, or removes a CLSID from the list.

## -parameters

### -param pluginType [in]

Member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_type">MF_Plugin_Type</a> enumeration, specifying the type of object.

### -param clsid [in]

The CLSID to add or remove.

### -param disabled [in]

Specifies whether to add or remove the CSLID. If the value is <b>TRUE</b>, the method adds the CLSID to the blocked list. Otherwise, the method removes it from the list.

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
The method succeeded.

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
</table>

## -remarks

The blocked list is global to the caller's process. Calling this method does not affect the list in other processes.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>
