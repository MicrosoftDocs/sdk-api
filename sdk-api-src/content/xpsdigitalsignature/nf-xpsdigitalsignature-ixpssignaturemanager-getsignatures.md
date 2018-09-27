---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.GetSignatures
title: IXpsSignatureManager::GetSignatures
author: windows-sdk-content
description: Gets a pointer to an IXpsSignatureCollection interface that contains a collection of XPS digital signatures.
old-location: xps\ixpssignaturemanager_getsignatures.htm
tech.root: printdocs
ms.assetid: 3a6a9a10-bc1d-45b8-a1b9-c7b725d9c13b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetSignatures, GetSignatures method [XPS Documents and Packaging], GetSignatures method [XPS Documents and Packaging],IXpsSignatureManager interface, IXpsSignatureManager interface [XPS Documents and Packaging],GetSignatures method, IXpsSignatureManager.GetSignatures, IXpsSignatureManager::GetSignatures, xps.ixpssignaturemanager_getsignatures, xpsdigitalsignature/IXpsSignatureManager::GetSignatures
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IXpsSignatureManager.GetSignatures
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureManager::GetSignatures


## -description


Gets a pointer to an <a href="https://msdn.microsoft.com/b8c46cc0-e071-4016-b658-1a5cd554a4c9">IXpsSignatureCollection</a> interface that contains a collection of XPS digital signatures.


## -parameters




### -param signatures [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/b8c46cc0-e071-4016-b658-1a5cd554a4c9">IXpsSignatureCollection</a> interface that contains a collection of XPS digital signatures.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a> and  <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
<i>signatures</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_PACKAGE_NOT_OPENED</b></dt>
</dl>
</td>
<td width="60%">
An XPS package has not yet been opened in the signature manager.

</td>
</tr>
</table>
 




## -remarks



The signature collection that is returned in <i>signatures</i> might include digital signatures that do not comply with the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.




## -see-also




<a href="https://msdn.microsoft.com/b8c46cc0-e071-4016-b658-1a5cd554a4c9">IXpsSignatureCollection</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

