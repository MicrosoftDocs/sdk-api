---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.SetSignatureOriginPartName
title: IXpsSignatureManager::SetSignatureOriginPartName (xpsdigitalsignature.h)
description: Sets the part name of the signature origin part.
helpviewer_keywords: ["IXpsSignatureManager interface [XPS Documents and Packaging]","SetSignatureOriginPartName method","IXpsSignatureManager.SetSignatureOriginPartName","IXpsSignatureManager::SetSignatureOriginPartName","SetSignatureOriginPartName","SetSignatureOriginPartName method [XPS Documents and Packaging]","SetSignatureOriginPartName method [XPS Documents and Packaging]","IXpsSignatureManager interface","xps.ixpssignaturemanager_setsignatureoriginpartname","xpsdigitalsignature/IXpsSignatureManager::SetSignatureOriginPartName"]
old-location: xps\ixpssignaturemanager_setsignatureoriginpartname.htm
tech.root: xps
ms.assetid: 686f31e1-3c61-449d-91f7-67f72d88a4b7
ms.date: 12/05/2018
ms.keywords: IXpsSignatureManager interface [XPS Documents and Packaging],SetSignatureOriginPartName method, IXpsSignatureManager.SetSignatureOriginPartName, IXpsSignatureManager::SetSignatureOriginPartName, SetSignatureOriginPartName, SetSignatureOriginPartName method [XPS Documents and Packaging], SetSignatureOriginPartName method [XPS Documents and Packaging],IXpsSignatureManager interface, xps.ixpssignaturemanager_setsignatureoriginpartname, xpsdigitalsignature/IXpsSignatureManager::SetSignatureOriginPartName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsSignatureManager::SetSignatureOriginPartName
 - xpsdigitalsignature/IXpsSignatureManager::SetSignatureOriginPartName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureManager.SetSignatureOriginPartName
---

# IXpsSignatureManager::SetSignatureOriginPartName


## -description

Sets the part name of the signature origin part.

## -parameters

### -param signatureOriginPartName [in]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the signature origin part.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code shown in the table that follows or an <b>HRESULT</b> error code that is returned by <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-setsignatureoriginpartname">IOpcDigitalSignatureManager::SetSignatureOriginPartName</a>.

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
<dt><b>XPS_E_PACKAGE_NOT_OPENED</b></dt>
</dl>
</td>
<td width="60%">
An XPS package was not loaded into the digital signature manager before calling this method.

</td>
</tr>
</table>

## -remarks

The part name cannot be set if any signatures exist.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>