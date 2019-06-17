---
UID: NF:oleauto.UnRegisterTypeLibForUser
title: UnRegisterTypeLibForUser function (oleauto.h)
author: windows-sdk-content
description: Removes type library information that was registered by using RegisterTypeLibForUser.
old-location: automat\unregistertypelibforuser.htm
tech.root: automat
ms.assetid: 2d88f97b-b1f6-4682-abf5-304ee752e2ae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UnRegisterTypeLibForUser, UnRegisterTypeLibForUser function [Automation], _oa96_UnRegisterTypeLibForUser, automat.unregistertypelibforuser, oleauto/UnRegisterTypeLibForUser
ms.topic: function
f1_keywords: ["oleauto/UnRegisterTypeLibForUser"]
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
 - UnRegisterTypeLibForUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UnRegisterTypeLibForUser function


## -description


Removes type library information that was registered by using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-registertypelibforuser">RegisterTypeLibForUser</a>.


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



Use <b>UnRegisterTypeLibForUser</b> to remove type library information for type libraries that were registered using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-registertypelibforuser">RegisterTypeLibForUser</a> function.



