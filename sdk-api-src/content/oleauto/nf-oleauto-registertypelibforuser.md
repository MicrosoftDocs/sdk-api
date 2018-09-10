---
UID: NF:oleauto.RegisterTypeLibForUser
title: RegisterTypeLibForUser function
author: windows-sdk-content
description: Registers a type library for use by the calling user.
old-location: automat\registertypelibforuser.htm
tech.root: automat
ms.assetid: ca8ae169-f849-4df2-8537-095d65ad6a08
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RegisterTypeLibForUser, RegisterTypeLibForUser function [Automation], _oa96_RegisterTypeLibForUser, automat.registertypelibforuser, oleauto/RegisterTypeLibForUser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - RegisterTypeLibForUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegisterTypeLibForUser function


## -description


Registers a type library for use by the calling user.


## -parameters




### -param ptlib

The type library.


### -param szFullPath [in]

The fully qualified path specification for the type library.


### -param szHelpDir [in, optional]

The directory in which the Help file for the library being registered can be found. This parameter can be null.



## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_IOERROR
</b></dt>
</dl>
</td>
<td width="60%">
The function could not write to the file.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_REGISTRYACCESS
</b></dt>
</dl>
</td>
<td width="60%">
The system registration database could not be opened.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE
</b></dt>
</dl>
</td>
<td width="60%">
The type library could not be opened.


</td>
</tr>
</table>
 




## -remarks



<b>RegisterTypeLibForUser</b> has functionality identical to <a href="https://msdn.microsoft.com/d0559a57-b1a4-4036-97ed-024d775cb595">RegisterTypeLib</a> except that type library is registered for use only by the calling user identity. 




