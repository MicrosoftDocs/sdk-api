---
UID: NF:strmif.IAMPluginControl.GetPreferredClsid
title: IAMPluginControl::GetPreferredClsid (strmif.h)
description: Searches the preferred list for a class identifier (CLSID) that matches a specified subtype.
helpviewer_keywords: ["GetPreferredClsid","GetPreferredClsid method [DirectShow]","GetPreferredClsid method [DirectShow]","IAMPluginControl interface","IAMPluginControl interface [DirectShow]","GetPreferredClsid method","IAMPluginControl.GetPreferredClsid","IAMPluginControl::GetPreferredClsid","dshow.iamplugincontrol_getpreferredclsid","strmif/IAMPluginControl::GetPreferredClsid"]
old-location: dshow\iamplugincontrol_getpreferredclsid.htm
tech.root: dshow
ms.assetid: 69f55810-9a3a-48cd-8fd2-d091a906d229
ms.date: 12/05/2018
ms.keywords: GetPreferredClsid, GetPreferredClsid method [DirectShow], GetPreferredClsid method [DirectShow],IAMPluginControl interface, IAMPluginControl interface [DirectShow],GetPreferredClsid method, IAMPluginControl.GetPreferredClsid, IAMPluginControl::GetPreferredClsid, dshow.iamplugincontrol_getpreferredclsid, strmif/IAMPluginControl::GetPreferredClsid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMPluginControl::GetPreferredClsid
 - strmif/IAMPluginControl::GetPreferredClsid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMPluginControl.GetPreferredClsid
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

<a href="/windows/desktop/api/strmif/nn-strmif-iamplugincontrol">IAMPluginControl</a>



<a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>