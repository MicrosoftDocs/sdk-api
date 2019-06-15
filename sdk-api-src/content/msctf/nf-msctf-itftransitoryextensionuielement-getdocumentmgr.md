---
UID: NF:msctf.ITfTransitoryExtensionUIElement.GetDocumentMgr
title: ITfTransitoryExtensionUIElement::GetDocumentMgr (msctf.h)
author: windows-sdk-content
description: The ITfTransitoryExtensionUIElement::GetDocumentMgr method returns the pointer of the transitory document manager.
old-location: tsf\itftransitoryextensionuielement_getdocumentmgr.htm
tech.root: TSF
ms.assetid: 199598fc-09e8-4d3b-b460-c76a1e4ee623
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDocumentMgr, GetDocumentMgr method [Text Services Framework], GetDocumentMgr method [Text Services Framework],ITfTransitoryExtensionUIElement interface, ITfTransitoryExtensionUIElement interface [Text Services Framework],GetDocumentMgr method, ITfTransitoryExtensionUIElement.GetDocumentMgr, ITfTransitoryExtensionUIElement::GetDocumentMgr, msctf/ITfTransitoryExtensionUIElement::GetDocumentMgr, tsf.itftransitoryextensionuielement_getdocumentmgr
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfTransitoryExtensionUIElement.GetDocumentMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfTransitoryExtensionUIElement::GetDocumentMgr


## -description


The <b>ITfTransitoryExtensionUIElement::GetDocumentMgr</b> method returns the pointer of the transitory document manager.


## -parameters




### -param ppdim [out]

[out] A pointer to receive the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a> interface pointer. This document manager object contains a context object that has the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface and contains the text of the transitory extension.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 



