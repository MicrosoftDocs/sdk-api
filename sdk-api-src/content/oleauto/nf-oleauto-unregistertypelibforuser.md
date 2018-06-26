---
UID: NF:oleauto.UnRegisterTypeLibForUser
title: UnRegisterTypeLibForUser function
author: windows-sdk-content
description: Removes type library information that was registered by using RegisterTypeLibForUser.
old-location: automat\unregistertypelibforuser.htm
old-project: automat
ms.assetid: 2d88f97b-b1f6-4682-abf5-304ee752e2ae
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: UnRegisterTypeLibForUser, UnRegisterTypeLibForUser function [Automation], _oa96_UnRegisterTypeLibForUser, automat.unregistertypelibforuser, oleauto/UnRegisterTypeLibForUser
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - UnRegisterTypeLibForUser
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# UnRegisterTypeLibForUser function


## -description


Removes type library information that was registered by using <a href="https://msdn.microsoft.com/ca8ae169-f849-4df2-8537-095d65ad6a08">RegisterTypeLibForUser</a>.


## -parameters




### -param libID

The GUID of the library.


### -param wMajorVerNum

The major version of the type library.


### -param wMinorVerNum

The minor version of the type library.


### -param lcid

The locale identifier.


### -param syskind

The target operating system.



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



Use <b>UnRegisterTypeLibForUser</b> to remove type library information for type libraries that were registered using the <a href="https://msdn.microsoft.com/ca8ae169-f849-4df2-8537-095d65ad6a08">RegisterTypeLibForUser</a> function.



