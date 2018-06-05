---
UID: NF:micaut.IMathInputControl.AddFunctionName
title: IMathInputControl::AddFunctionName
author: windows-sdk-content
description: Adds a new function-name definition to the list of custom math functions that the recognizer accepts.
old-location: tablet\imathinputcontrol_addfunctionname.htm
old-project: tablet
ms.assetid: eb1c9172-b520-4f6e-ae15-52634aa30007
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: AddFunctionName, AddFunctionName method [Tablet PC], AddFunctionName method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],AddFunctionName method, IMathInputControl.AddFunctionName, IMathInputControl::AddFunctionName, micaut/IMathInputControl::AddFunctionName, tablet.imathinputcontrol_addfunctionname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	micaut.h
api_name:
-	IMathInputControl.AddFunctionName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMathInputControl::AddFunctionName


## -description


Adds a new function-name definition to the list of custom math functions that the recognizer accepts.


## -parameters




### -param FunctionName






#### - FunctonName [in]

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




<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>



<a href="https://msdn.microsoft.com/7c1a16c7-4490-480d-9831-ca297ccdde80">RemoveFunctionName</a>
 

 

