---
UID: NF:ndhelper.INetDiagHelper.GetAttributes
title: INetDiagHelper::GetAttributes (ndhelper.h)
description: Retrieves additional information about a problem that the helper class extension has diagnosed.
helpviewer_keywords: ["GetAttributes","GetAttributes method [NDF]","GetAttributes method [NDF]","INetDiagHelper interface","INetDiagHelper interface [NDF]","GetAttributes method","INetDiagHelper.GetAttributes","INetDiagHelper::GetAttributes","ndf.inetdiaghelpe_getattributes","ndhelper/INetDiagHelper::GetAttributes"]
old-location: ndf\inetdiaghelpe_getattributes.htm
tech.root: NDF
ms.assetid: 4f1f371a-853f-4022-808b-eea01aee4a52
ms.date: 12/05/2018
ms.keywords: GetAttributes, GetAttributes method [NDF], GetAttributes method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],GetAttributes method, INetDiagHelper.GetAttributes, INetDiagHelper::GetAttributes, ndf.inetdiaghelpe_getattributes, ndhelper/INetDiagHelper::GetAttributes
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
 - INetDiagHelper::GetAttributes
 - ndhelper/INetDiagHelper::GetAttributes
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
 - INetDiagHelper.GetAttributes
---

# INetDiagHelper::GetAttributes


## -description

The <b>GetAttributes</b> method retrieves additional information about a problem that the helper class extension has diagnosed.

## -parameters

### -param pcelt [out]

A pointer to a count of elements in the <b>HELPER_ATTRIBUTE</b> array.

### -param pprgAttributes [out]

A pointer to an array of <a href="/windows/desktop/api/ndattrib/ns-ndattrib-helper_attribute">HELPER_ATTRIBUTE</a> structures.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This optional method is not implemented.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The diagnosis or repair operation has been canceled.

</td>
</tr>
</table>
 

Helper Class Extensions may return HRESULTS that are specific to the failures encountered in the function.

## -remarks

This method is not required when building a Helper Class Extension.

During the process of diagnosis and repair, a helper class may optionally return attributes to NDF that improve NDF's handling of the diagnosis.  The predefined attributes that can be returned to NDF are as follows.




<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="werperameter__Type__AT_UINT32_"></a><a id="werperameter__type__at_uint32_"></a><a id="WERPERAMETER__TYPE__AT_UINT32_"></a> werperameter (Type: AT_UINT32)

</td>
<td width="60%">
When diagnosis fails, an optional attribute for additional helper class specific Windows Error Reporting (WER) bucketing parameter.

</td>
</tr>
<tr>
<td width="40%">
<a id="werfile__Type__AT_STRING_"></a><a id="werfile__type__at_string_"></a><a id="WERFILE__TYPE__AT_STRING_"></a> werfile (Type: AT_STRING)

</td>
<td width="60%">
An optional attribute for adding helper class-specific files to Windows Error Reporting (WER) reports.

</td>
</tr>
<tr>
<td width="40%">
<a id="rootcauseid__Type__AT_GUID_"></a><a id="rootcauseid__type__at_guid_"></a><a id="ROOTCAUSEID__TYPE__AT_GUID_"></a> rootcauseid (Type: AT_GUID)

</td>
<td width="60%">
Helper Classes can often diagnose more than one problem at once.  Analysis of the problem encountered can be improved in NDF if the extension returns a HelperAttribute of type AT_GUID with the pszName parameter set to rootcauseid and the Guid field set to a GUID identifying the specific problem encountered.  These GUIDs are custom defined by the helper extension.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a>