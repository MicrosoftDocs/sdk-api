---
UID: NF:ndhelper.INetDiagHelperInfo.GetAttributeInfo
title: INetDiagHelperInfo::GetAttributeInfo (ndhelper.h)
description: The GetAttributeInfo method retrieves the list of key parameters needed by the Helper Class Extension.
helpviewer_keywords: ["GetAttributeInfo","GetAttributeInfo method [NDF]","GetAttributeInfo method [NDF]","INetDiagHelperInfo interface","INetDiagHelperInfo interface [NDF]","GetAttributeInfo method","INetDiagHelperInfo.GetAttributeInfo","INetDiagHelperInfo::GetAttributeInfo","ndf.inetdiaghelperinfo_getattributeinfo","ndhelper/INetDiagHelperInfo::GetAttributeInfo"]
old-location: ndf\inetdiaghelperinfo_getattributeinfo.htm
tech.root: NDF
ms.assetid: 0c1a12f3-357f-4d96-b0ef-99d788b6e020
ms.date: 12/05/2018
ms.keywords: GetAttributeInfo, GetAttributeInfo method [NDF], GetAttributeInfo method [NDF],INetDiagHelperInfo interface, INetDiagHelperInfo interface [NDF],GetAttributeInfo method, INetDiagHelperInfo.GetAttributeInfo, INetDiagHelperInfo::GetAttributeInfo, ndf.inetdiaghelperinfo_getattributeinfo, ndhelper/INetDiagHelperInfo::GetAttributeInfo
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - INetDiagHelperInfo::GetAttributeInfo
 - ndhelper/INetDiagHelperInfo::GetAttributeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ndhelper.h
api_name:
 - INetDiagHelperInfo.GetAttributeInfo
---

# INetDiagHelperInfo::GetAttributeInfo


## -description

The <b>GetAttributeInfo</b> method retrieves the list of key parameters needed by the Helper Class Extension.

## -parameters

### -param pcelt [out]

A pointer to a count of elements in the array pointed to by <i>pprgAttributeInfos</i>.

### -param pprgAttributeInfos [out]

A pointer to an array of <a href="/windows/desktop/api/ndhelper/ns-ndhelper-helperattributeinfo">HelperAttributeInfo</a> structures that contain helper class key parameters.

## -returns

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
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters has not been provided correctly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges to perform the diagnosis or repair operation.

</td>
</tr>
</table>
 

Helper Class Extensions may return HRESULTS that are specific to the diagnoses or repairs.

## -remarks

The key parameter list is used by NDF to determine whether enough information is available for the extension to perform diagnosis.  If the hypothesis to call the extension lacks a key attribute, the extension will not be called.  Optional attributes will not be returned by this call.

## -see-also

<a href="/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo">INetDiagHelperInfo</a>