---
UID: NF:msctf.ITfDisplayAttributeMgr.GetDisplayAttributeInfo
title: ITfDisplayAttributeMgr::GetDisplayAttributeInfo (msctf.h)
description: ITfDisplayAttributeMgr::GetDisplayAttributeInfo method
helpviewer_keywords: ["GetDisplayAttributeInfo","GetDisplayAttributeInfo method [Text Services Framework]","GetDisplayAttributeInfo method [Text Services Framework]","ITfDisplayAttributeMgr interface","ITfDisplayAttributeMgr interface [Text Services Framework]","GetDisplayAttributeInfo method","ITfDisplayAttributeMgr.GetDisplayAttributeInfo","ITfDisplayAttributeMgr::GetDisplayAttributeInfo","_tsf_itfdisplayattributemgr_getdisplayattributeinfo_ref","msctf/ITfDisplayAttributeMgr::GetDisplayAttributeInfo","tsf.itfdisplayattributemgr_getdisplayattributeinfo"]
old-location: tsf\itfdisplayattributemgr_getdisplayattributeinfo.htm
tech.root: TSF
ms.assetid: 41bc183f-013f-4e68-bb72-d9a30d5ea48e
ms.date: 12/05/2018
ms.keywords: GetDisplayAttributeInfo, GetDisplayAttributeInfo method [Text Services Framework], GetDisplayAttributeInfo method [Text Services Framework],ITfDisplayAttributeMgr interface, ITfDisplayAttributeMgr interface [Text Services Framework],GetDisplayAttributeInfo method, ITfDisplayAttributeMgr.GetDisplayAttributeInfo, ITfDisplayAttributeMgr::GetDisplayAttributeInfo, _tsf_itfdisplayattributemgr_getdisplayattributeinfo_ref, msctf/ITfDisplayAttributeMgr::GetDisplayAttributeInfo, tsf.itfdisplayattributemgr_getdisplayattributeinfo
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfDisplayAttributeMgr::GetDisplayAttributeInfo
 - msctf/ITfDisplayAttributeMgr::GetDisplayAttributeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfDisplayAttributeMgr.GetDisplayAttributeInfo
---

# ITfDisplayAttributeMgr::GetDisplayAttributeInfo


## -description

Obtains a display attribute data object.

## -parameters

### -param guid [in]

Contains a GUID that identifies the display attribute data requested. This value is obtained by obtaining the GUID_PROP_ATTRIBUTE property for the range of text. For more information, see <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty">ITfContext::GetProperty</a> and <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-trackproperties">ITfContext::TrackProperties</a>.

### -param ppInfo [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfdisplayattributeinfo">ITfDisplayAttributeInfo</a> interface pointer that receives the object.

### -param pclsidOwner [out]

Pointer to a CLSID value that receives the CLSID of the display attribute provider. This parameter can be <b>NULL</b> if the CLSID is not required.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -see-also

[ITfDisplayAttributeMgr interface](nn-msctf-itfdisplayattributemgr.md), [IEnumTfDisplayAttributeInfo interface](nn-msctf-ienumtfdisplayattributeinfo.md), [ITfContext::GetProperty](nf-msctf-itfcontext-getproperty.md), [ITfContext::TrackProperties](nf-msctf-itfcontext-trackproperties.md)