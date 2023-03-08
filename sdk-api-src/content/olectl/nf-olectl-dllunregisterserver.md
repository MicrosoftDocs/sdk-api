---
UID: NF:olectl.DllUnregisterServer
title: DllUnregisterServer function (olectl.h)
description: Instructs an in-process server to remove only those entries created through DllRegisterServer.
helpviewer_keywords: ["DllUnregisterServer","DllUnregisterServer function [COM]","_com_DllUnregisterServer","com.dllunregisterserver","olectl/DllUnregisterServer"]
old-location: com\dllunregisterserver.htm
tech.root: com
ms.assetid: b71137a7-284e-4521-a3b2-9dad9c9d3c54
ms.date: 12/05/2018
ms.keywords: DllUnregisterServer, DllUnregisterServer function [COM], _com_DllUnregisterServer, com.dllunregisterserver, olectl/DllUnregisterServer
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DllUnregisterServer
 - olectl/DllUnregisterServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - DllUnregisterServer
---

# DllUnregisterServer function


## -description

Instructs an in-process server to remove only those entries created through <a href="/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a>.



## -returns

This function can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The registry entries were deleted successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Unregistration of this server's known entries was successful, but other entries still exist for this server's classes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SELFREG_E_TYPELIB</b></dt>
</dl>
</td>
<td width="60%">
The server was unable to remove the entries of all the type libraries used by its classes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SELFREG_E_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The server was unable to remove the entries of all the object classes.

</td>
</tr>
</table>

## -remarks

The server must not disturb any entries that it did not create which currently exist for its object classes. For example, between registration and unregistration, the user may have specified a Treat As relationship between this class and another. In that case, unregistration can remove all entries except the <b>TreatAs</b> key and any others that were not explicitly created in <a href="/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a>. The <a href="/windows/desktop/SysInfo/registry-functions">registry functions</a> specifically disallow the deletion of an entire populated tree in the registry. The server can attempt, as the last step, to remove the CLSID key, but if other entries still exist, the key will remain.

## -see-also

<a href="/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a>
