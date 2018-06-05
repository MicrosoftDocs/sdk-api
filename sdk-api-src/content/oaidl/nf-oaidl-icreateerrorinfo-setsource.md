---
UID: NF:oaidl.ICreateErrorInfo.SetSource
title: ICreateErrorInfo::SetSource
author: windows-sdk-content
description: Sets the language-dependent programmatic identifier (ProgID) for the class or application that raised the error.
old-location: automat\icreateerrorinfo_setsource.htm
old-project: automat
ms.assetid: 7f0e6349-9d31-4ab6-9a91-3822e81188e5
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: ICreateErrorInfo interface [Automation],SetSource method, ICreateErrorInfo.SetSource, ICreateErrorInfo::SetSource, SetSource, SetSource method [Automation], SetSource method [Automation],ICreateErrorInfo interface, _oa96_ICreateErrorInfo_SetSource, automat.icreateerrorinfo_setsource, oaidl/ICreateErrorInfo::SetSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VARKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	oaidl.h
api_name:
-	ICreateErrorInfo.SetSource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ICreateErrorInfo::SetSource


## -description


Sets the language-dependent programmatic identifier (ProgID) for the class or application that raised the error.


## -parameters




### -param szSource [in]

A ProgID in the form <i>progname</i>.<i>objectname</i>.



## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.


</td>
</tr>
</table>
 




## -remarks



This method should be used to identify the class or application that is the source of the error. The language for the returned ProgID depends on the locale identifier (LCID) that was passed to the method at the time of invocation.



Use of this function is demonstrated in the file Main.cpp of the COM Fundamentals Hello sample.




## -see-also




<a href="https://msdn.microsoft.com/2e7c5ad5-9018-413e-8826-ef752ebf302c">ICreateErrorInfo</a>
 

 

