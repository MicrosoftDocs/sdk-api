---
UID: NF:shlwapi.SHLoadIndirectString
title: SHLoadIndirectString function (shlwapi.h)
description: Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol).
helpviewer_keywords: ["SHLoadIndirectString","SHLoadIndirectString function [Windows Shell]","_shell_SHLoadIndirectString","shell.SHLoadIndirectString","shlwapi/SHLoadIndirectString"]
old-location: shell\SHLoadIndirectString.htm
tech.root: shell
ms.assetid: f0265cd8-deb8-4bca-b379-39aff49c7df1
ms.date: 12/05/2018
ms.keywords: SHLoadIndirectString, SHLoadIndirectString function [Windows Shell], _shell_SHLoadIndirectString, shell.SHLoadIndirectString, shlwapi/SHLoadIndirectString
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.5 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHLoadIndirectString
 - shlwapi/SHLoadIndirectString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-String-l2-1-1.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - SHLoadIndirectString
---

# SHLoadIndirectString function


## -description

Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol).

## -parameters

### -param pszSource [in]

Type: <b>PCWSTR</b>

A pointer to a buffer that contains the indirect string from which the resource will be retrieved. This string should begin with the '@' symbol and use one of the forms discussed in the Remarks section. This function will successfully accept a string that does not begin with an '@' symbol, but the string will be simply passed unchanged to <i>pszOutBuf</i>.

### -param pszOutBuf [out]

Type: <b>PWSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the text resource. Both <i>pszOutBuf</i> and <i>pszSource</i> can point to the same buffer, in which case the original string will be overwritten.

### -param cchOutBuf [in]

Type: <b>UINT</b>

The size of the buffer pointed to by <i>pszOutBuf</i>, in characters.

### -param ppvReserved

Type: <b>void**</b>

Not used; set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An indirect string can be provided in several forms, each of which has its own interpretation:
            
			    

<ul>
<li><b>File name and resource ID</b>
``` syntax
@filename,resource
```

The string is extracted from the file named, using the <i>resource</i> value as a locator. If the resource value is zero or greater, the number becomes the index of the string in the binary file. If the number is negative, it becomes a resource ID. The retrieved string is copied to the output buffer and the function returns S_OK.

</li>
<li><b>File name and resource ID with a version modifier</b>
``` syntax
@filename,resource;v2
```

This form can be used when a resource is changed but still uses the same index or ID as the old resource. Without a version modifier, the Multilingual User Interface (MUI) cache will not recognize that the resource has changed and will not refresh. By appending the version modifier, the value is seen as a new resource and is added to the cache. Note that it is recommended that you use a new ID or index for a new resource, and use a version modifier only when that is not possible.

</li>
<li><b>PRI file path and resource ID</b>
``` syntax
@{PRIFilepath?resource}
```

The Package Resource Index (PRI) is a binary format introduced in Windows 8 that contains indexed resources or references to resources. The .pri file is bundled as part of an app's package. For more information on .pri files, see <a href="/previous-versions/hh694557(v=vs.110)">Creating and retrieving resources in Windows Store apps</a>.

The string is extracted from the .pri file named, using the <i>resource</i> as a locator. The retrieved string is copied to the output buffer and the function returns S_OK. The string is extracted based on the current Shell environment or <a href="/uwp/api/windows.applicationmodel.resources.core.resourcecontext">ResourceContext</a>.

An example of this type of indirect string is shown here.
                        
                            


```

@{C:\Program Files\WindowsApps\Microsoft.Camera_6.2.8376.0_x64__8wekyb3d8bbwe\resources.pri? ms-resource://Microsoft.Camera/resources/manifestAppDescription}
```




</li>
<li><b>Package name and resource ID</b>
``` syntax
@{PackageFullName?resource}
```

The string is extracted from the Resources.pri file stored in the app's root directory of the package identified by <i>PackageFullName</i>, using the <i>resource</i> as a locator. The retrieved string is copied to the output buffer and the function returns S_OK. The string is extracted based on the app's environment or <a href="/uwp/api/windows.applicationmodel.resources.core.resourcecontext">ResourceContext</a>.

<div class="alert"><b>Note</b>  This string must refer to a package installed for the current user. If it does not, the call will fail.</div>
<div> </div>
An example of this type of indirect string is shown here. In this example, the reference name is fully-qualified, but it contains no namespace (for example, "resources"). The deployment stack expands the name to look for it in all namespaces.


```

@{Microsoft.Camera_6.2.8376.0_x64__8wekyb3d8bbwe? ms-resource://Microsoft.Camera/manifestAppDescription}
```




In this next example, the fully-qualified reference name does specify a namespace to limit the lookup to.


```

@{Microsoft.Camera_6.2.8376.0_x64__8wekyb3d8bbwe? ms-resource://Microsoft.Camera/resources/manifestAppDescription}
```




</li>
</ul>
If the string is not an indirect string, then the string is directly copied without change to <i>pszOutBuf</i> and the function returns S_OK.
