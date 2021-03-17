---
UID: NF:comppkgsup.InstantiateComponentFromPackage
title: InstantiateComponentFromPackage function (comppkgsup.h)
description: Creates an instance of a class in an application package.
helpviewer_keywords: ["InstantiateComponentFromPackage","InstantiateComponentFromPackage function [Windows API]","comppkgsup/InstantiateComponentFromPackage","winprog.instantiatecomponentfrompackage"]
old-location: winprog\instantiatecomponentfrompackage.htm
tech.root: winprog
ms.assetid: 831324BC-854B-4070-9DAE-55E68304D608
ms.date: 12/05/2018
ms.keywords: InstantiateComponentFromPackage, InstantiateComponentFromPackage function [Windows API], comppkgsup/InstantiateComponentFromPackage, winprog.instantiatecomponentfrompackage
req.header: comppkgsup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comppkgsup.lib
req.dll: CompPkgSup.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InstantiateComponentFromPackage
 - comppkgsup/InstantiateComponentFromPackage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CompPkgSup.dll
api_name:
 - InstantiateComponentFromPackage
---

# InstantiateComponentFromPackage function


## -description

Creates an instance of a class in an application package.

## -parameters

### -param classId [in]

The  class to activate in the named package.

### -param packageFullName [in]

The full name of the package.

### -param instance [out]

Receives an instance of the class.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The class is not registered or the class is not listed under the registry key "HKEY_LOCAL_MACHINE\Software\Microsoft\MediaEngine\MediaExtensions\EME\CDMS". See remarks for more info.

</td>
</tr>
</table>

## -remarks

This function can only be used with packages whose "PackageFamilyName"  is defined as a subkey key that is registered under the "HKEY_LOCAL_MACHINE\Software\Microsoft\MediaEngine\MediaExtensions\EME\CDMS" key. 

 This API should only be called in very exceptional circumstances because code installed from the application store should not be invoked from desktop applications as it is has a lower level of trust associated with it.

