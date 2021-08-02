---
UID: NF:oaidl.ISupportErrorInfo.InterfaceSupportsErrorInfo
title: ISupportErrorInfo::InterfaceSupportsErrorInfo (oaidl.h)
description: Indicates whether an interface supports the IErrorInfo interface.
helpviewer_keywords: ["ISupportErrorInfo interface [Automation]","InterfaceSupportsErrorInfo method","ISupportErrorInfo.InterfaceSupportsErrorInfo","ISupportErrorInfo::InterfaceSupportsErrorInfo","InterfaceSupportsErrorInfo","InterfaceSupportsErrorInfo method [Automation]","InterfaceSupportsErrorInfo method [Automation]","ISupportErrorInfo interface","_oa96_ISupportErrorInfo_InterfaceSupportsErrorInfo","automat.isupporterrorinfo_interfacesupportserrorinfo","oaidl/ISupportErrorInfo::InterfaceSupportsErrorInfo"]
old-location: automat\isupporterrorinfo_interfacesupportserrorinfo.htm
tech.root: automat
ms.assetid: a54ef18d-ee3f-4483-ac4a-99d758f0960a
ms.date: 12/05/2018
ms.keywords: ISupportErrorInfo interface [Automation],InterfaceSupportsErrorInfo method, ISupportErrorInfo.InterfaceSupportsErrorInfo, ISupportErrorInfo::InterfaceSupportsErrorInfo, InterfaceSupportsErrorInfo, InterfaceSupportsErrorInfo method [Automation], InterfaceSupportsErrorInfo method [Automation],ISupportErrorInfo interface, _oa96_ISupportErrorInfo_InterfaceSupportsErrorInfo, automat.isupporterrorinfo_interfacesupportserrorinfo, oaidl/ISupportErrorInfo::InterfaceSupportsErrorInfo
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - ISupportErrorInfo::InterfaceSupportsErrorInfo
 - oaidl/ISupportErrorInfo::InterfaceSupportsErrorInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ISupportErrorInfo.InterfaceSupportsErrorInfo
---

# ISupportErrorInfo::InterfaceSupportsErrorInfo


## -description

Indicates whether an interface supports the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a> interface.

## -parameters

### -param riid [in]

An interface identifier (IID).

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
The interface supports <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The interface does not support <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a>.

</td>
</tr>
</table>

## -remarks

Objects that support the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a> interface must also implement this interface.



Programs that receive an error return value should call <b>QueryInterface</b> to get a pointer to the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-isupporterrorinfo">ISupportErrorInfo</a> interface, and then call <b>InterfaceSupportsErrorInfo</b> with the <i>riid</i> of the interface that returned the return value. If <b>InterfaceSupportsErrorInfo</b> returns S_FALSE, then the error object does not represent an error returned from the caller, but from somewhere else. In this case, the error object can be considered incorrect and should be discarded.



If <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-isupporterrorinfo">ISupportErrorInfo</a> returns S_OK, use the <a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a> function to get a pointer to the error object.



For an example that demonstrates implementing <b>InterfaceSupportsErrorInfo</b>, see the ErrorInfo.cpp file in the COM Fundamentals Lines sample.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-isupporterrorinfo">ISupportErrorInfo</a>