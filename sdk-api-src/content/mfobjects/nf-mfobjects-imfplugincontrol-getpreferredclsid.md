---
UID: NF:mfobjects.IMFPluginControl.GetPreferredClsid
title: IMFPluginControl::GetPreferredClsid (mfobjects.h)
description: Searches the preferred list for a class identifier (CLSID) that matches a specified key name.
helpviewer_keywords: ["GetPreferredClsid","GetPreferredClsid method [Media Foundation]","GetPreferredClsid method [Media Foundation]","IMFPluginControl interface","IMFPluginControl interface [Media Foundation]","GetPreferredClsid method","IMFPluginControl.GetPreferredClsid","IMFPluginControl::GetPreferredClsid","mf.imfplugincontrol_imfplugincontrol__getpreferredclsid","mfobjects/IMFPluginControl::GetPreferredClsid"]
old-location: mf\imfplugincontrol_imfplugincontrol__getpreferredclsid.htm
tech.root: mf
ms.assetid: c78843ed-b666-4b81-a7ed-66e514d0d342
ms.date: 12/05/2018
ms.keywords: GetPreferredClsid, GetPreferredClsid method [Media Foundation], GetPreferredClsid method [Media Foundation],IMFPluginControl interface, IMFPluginControl interface [Media Foundation],GetPreferredClsid method, IMFPluginControl.GetPreferredClsid, IMFPluginControl::GetPreferredClsid, mf.imfplugincontrol_imfplugincontrol__getpreferredclsid, mfobjects/IMFPluginControl::GetPreferredClsid
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
 - IMFPluginControl::GetPreferredClsid
 - mfobjects/IMFPluginControl::GetPreferredClsid
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
 - IMFPluginControl.GetPreferredClsid
---

# IMFPluginControl::GetPreferredClsid


## -description

Searches the preferred list for a class identifier (CLSID) that matches a specified key name.

## -parameters

### -param pluginType [in]

Member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_type">MF_Plugin_Type</a> enumeration, specifying the type of object.

### -param selector [in]

The key name to match. For more information about the format of key names, see the Remarks section of <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>.

### -param clsid [out]

Receives a CLSID from the preferred list.

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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
No CLSID matching this key was found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>