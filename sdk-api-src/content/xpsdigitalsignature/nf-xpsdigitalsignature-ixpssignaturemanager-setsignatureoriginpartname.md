---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.SetSignatureOriginPartName
title: IXpsSignatureManager::SetSignatureOriginPartName
author: windows-sdk-content
description: Sets the part name of the signature origin part.
old-location: xps\ixpssignaturemanager_setsignatureoriginpartname.htm
old-project: printdocs
ms.assetid: 686f31e1-3c61-449d-91f7-67f72d88a4b7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsSignatureManager interface [XPS Documents and Packaging],SetSignatureOriginPartName method, IXpsSignatureManager.SetSignatureOriginPartName, IXpsSignatureManager::SetSignatureOriginPartName, SetSignatureOriginPartName, SetSignatureOriginPartName method [XPS Documents and Packaging], SetSignatureOriginPartName method [XPS Documents and Packaging],IXpsSignatureManager interface, xps.ixpssignaturemanager_setsignatureoriginpartname, xpsdigitalsignature/IXpsSignatureManager::SetSignatureOriginPartName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsdigitalsignature.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XPS_SIGN_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureManager.SetSignatureOriginPartName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignatureManager::SetSignatureOriginPartName


## -description


Sets the part name of the signature origin part.


## -parameters




### -param signatureOriginPartName [in]

A pointer to an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name of the signature origin part.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code shown in the table that follows or an <b>HRESULT</b> error code that is returned by <a href="https://msdn.microsoft.com/edf1590c-14a2-4887-a2df-20b5b4cb89a6">IOpcDigitalSignatureManager::SetSignatureOriginPartName</a>.

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




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

