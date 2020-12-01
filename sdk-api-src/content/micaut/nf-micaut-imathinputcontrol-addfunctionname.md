---
UID: NF:micaut.IMathInputControl.AddFunctionName
title: IMathInputControl::AddFunctionName (micaut.h)
description: Adds a new function-name definition to the list of custom math functions that the recognizer accepts.
helpviewer_keywords: ["AddFunctionName","AddFunctionName method [Tablet PC]","AddFunctionName method [Tablet PC]","IMathInputControl interface","IMathInputControl interface [Tablet PC]","AddFunctionName method","IMathInputControl.AddFunctionName","IMathInputControl::AddFunctionName","micaut/IMathInputControl::AddFunctionName","tablet.imathinputcontrol_addfunctionname"]
old-location: tablet\imathinputcontrol_addfunctionname.htm
tech.root: tablet
ms.assetid: eb1c9172-b520-4f6e-ae15-52634aa30007
ms.date: 12/05/2018
ms.keywords: AddFunctionName, AddFunctionName method [Tablet PC], AddFunctionName method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],AddFunctionName method, IMathInputControl.AddFunctionName, IMathInputControl::AddFunctionName, micaut/IMathInputControl::AddFunctionName, tablet.imathinputcontrol_addfunctionname
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
 - IMathInputControl::AddFunctionName
 - micaut/IMathInputControl::AddFunctionName
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
 - IMathInputControl.AddFunctionName
---

# IMathInputControl::AddFunctionName


## -description

Adds a new function-name definition to the list of custom math functions that the recognizer accepts.

## -parameters

### -param FunctionName [in]

The name of the function to be added.

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
The name could not be added.

</td>
</tr>
</table>

## -remarks

This function is used to add custom math functions that do not exist in the default dictionary. After a function has been added to the dictionary of functions, the recognizer will be able to read it; however, a custom function name may be recognizable only letter by letter rather than as a whole word in cursive.

## -see-also

<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>



<a href="/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-removefunctionname">RemoveFunctionName</a>