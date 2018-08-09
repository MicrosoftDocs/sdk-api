---
UID: NF:oaidl.ICreateTypeLib.SetHelpContext
title: ICreateTypeLib::SetHelpContext
author: windows-sdk-content
description: Sets the Help context ID for retrieving general Help information for the type library.
old-location: automat\icreatetypelib_sethelpcontext.htm
old-project: automat
ms.assetid: 58d7cd77-cfb6-493e-a9fd-26f469eec9f0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICreateTypeLib interface [Automation],SetHelpContext method, ICreateTypeLib.SetHelpContext, ICreateTypeLib::SetHelpContext, SetHelpContext, SetHelpContext method [Automation], SetHelpContext method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SetHelpContext, automat.icreatetypelib_sethelpcontext, oaidl/ICreateTypeLib::SetHelpContext
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateTypeLib.SetHelpContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICreateTypeLib::SetHelpContext


## -description


Sets the Help context ID for retrieving general Help information for the type library.


## -parameters




### -param dwHelpContext [in]

The Help context ID.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

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
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.

</td>
</tr>
</table>
 




## -remarks



Calling <b>SetHelpContext</b> with a Help context of zero is equivalent to not calling it at all, because zero indicates a null Help context.




## -see-also




<a href="https://msdn.microsoft.com/d245cd25-ce31-42da-a42d-dc412d5b98e7">ICreateTypeLib</a>
 

 

