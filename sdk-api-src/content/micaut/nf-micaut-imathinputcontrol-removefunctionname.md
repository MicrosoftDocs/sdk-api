---
UID: NF:micaut.IMathInputControl.RemoveFunctionName
title: IMathInputControl::RemoveFunctionName (micaut.h)
description: Removes a function-name definition from the list of custom math functions that the recognizer accepts.
helpviewer_keywords: ["IMathInputControl interface [Tablet PC]","RemoveFunctionName method","IMathInputControl.RemoveFunctionName","IMathInputControl::RemoveFunctionName","RemoveFunctionName","RemoveFunctionName method [Tablet PC]","RemoveFunctionName method [Tablet PC]","IMathInputControl interface","micaut/IMathInputControl::RemoveFunctionName","tablet.imathinputcontrol_removefunctionname"]
old-location: tablet\imathinputcontrol_removefunctionname.htm
tech.root: tablet
ms.assetid: 7c1a16c7-4490-480d-9831-ca297ccdde80
ms.date: 12/05/2018
ms.keywords: IMathInputControl interface [Tablet PC],RemoveFunctionName method, IMathInputControl.RemoveFunctionName, IMathInputControl::RemoveFunctionName, RemoveFunctionName, RemoveFunctionName method [Tablet PC], RemoveFunctionName method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::RemoveFunctionName, tablet.imathinputcontrol_removefunctionname
req.header: micaut.h
req.include-header: Micaut.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Micaut.idl
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
 - IMathInputControl::RemoveFunctionName
 - micaut/IMathInputControl::RemoveFunctionName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl.RemoveFunctionName
---

# IMathInputControl::RemoveFunctionName


## -description

Removes a function-name definition from the list of custom math functions that the recognizer accepts.

## -parameters

### -param FunctionName

The name of the function to remove.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The named math function cannot be removed because it is not in the list of custom math functions that the recognizer accepts.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-addfunctionname">AddFunctionName</a>



<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>