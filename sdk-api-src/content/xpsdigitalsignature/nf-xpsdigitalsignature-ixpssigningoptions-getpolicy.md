---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetPolicy
title: IXpsSigningOptions::GetPolicy (xpsdigitalsignature.h)
author: windows-sdk-content
description: Gets the XPS_SIGN_POLICY value that specifies the signing policy.
old-location: xps\ixpssigningoptions_getpolicy.htm
tech.root: printdocs
ms.assetid: 0643ee4d-7991-4570-8dce-8166f007abc8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPolicy, GetPolicy method [XPS Documents and Packaging], GetPolicy method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetPolicy method, IXpsSigningOptions.GetPolicy, IXpsSigningOptions::GetPolicy, xps.ixpssigningoptions_getpolicy, xpsdigitalsignature/IXpsSigningOptions::GetPolicy
ms.topic: method
f1_keywords: 
 - "xpsdigitalsignature/IXpsSigningOptions.GetPolicy"
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
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
 - xpsdigitalsignature.h
api_name:
 - IXpsSigningOptions.GetPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSigningOptions::GetPolicy


## -description


Gets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/ne-xpsdigitalsignature-__midl___midl_itf_xpsdigitalsignature_0000_0000_0002">XPS_SIGN_POLICY</a> value that specifies the signing policy.


## -parameters




### -param policy [out, retval]

The logical <b>OR</b> of the <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/ne-xpsdigitalsignature-__midl___midl_itf_xpsdigitalsignature_0000_0000_0002">XPS_SIGN_POLICY</a> value that specifies the signing policy.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a> and  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>policy</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
 The interface is not connected to the signature manager.

</td>
</tr>
</table>
 




## -remarks



If the  <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/ne-xpsdigitalsignature-__midl___midl_itf_xpsdigitalsignature_0000_0000_0002">XPS_SIGN_POLICY</a> value is set but does not have a  corresponding part in the package being signed, only the  relationship type will be signed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/ne-xpsdigitalsignature-__midl___midl_itf_xpsdigitalsignature_0000_0000_0002">XPS_SIGN_POLICY</a>
 

 

