---
UID: NF:oleauto.UnRegisterTypeLib
title: UnRegisterTypeLib function
author: windows-driver-content
description: Removes type library information from the system registry. Use this API to allow applications to properly uninstall themselves.
old-location: automat\unregistertypelib.htm
old-project: automat
ms.assetid: 36c763f0-562c-4fc8-9449-b37e993d5f5c
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: UnRegisterTypeLib, UnRegisterTypeLib function [Automation], _oa96_UnRegisterTypeLib, automat.unregistertypelib, oleauto/UnRegisterTypeLib
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
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	UnRegisterTypeLib
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# UnRegisterTypeLib function


## -description


Removes type library information from the system registry. Use this API to allow applications to properly uninstall themselves.


## -parameters




### -param libID

The GUID of the type library.


### -param wVerMajor

The major version of the type library.


### -param wVerMinor

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



In-process objects typically call this API from <b>DllUnregisterServer</b>. 




