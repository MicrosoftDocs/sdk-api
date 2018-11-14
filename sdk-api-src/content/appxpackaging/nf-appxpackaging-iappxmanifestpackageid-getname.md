---
UID: NF:appxpackaging.IAppxManifestPackageId.GetName
title: IAppxManifestPackageId::GetName
author: windows-sdk-content
description: Gets the name of the package as defined in the manifest.
old-location: appxpkg\iappxmanifestpackageid_getname.htm
tech.root: appxpkg
ms.assetid: F59FDC61-BA78-4204-AAD3-C34B7F1EB37B
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetName, GetName method [App packaging and management], GetName method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetName method, IAppxManifestPackageId.GetName, IAppxManifestPackageId::GetName, appxpackaging/IAppxManifestPackageId::GetName, appxpkg.iappxmanifestpackageid_getname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxManifestPackageId.GetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- appxpackaging.h
: 
- IAppxManifestPackageId.GetName
: 
---

# IAppxManifestPackageId::GetName


## -description


Gets the name of the package as defined in the manifest.


## -parameters




### -param name [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

The name of the package.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -remarks



Package name information is specified using the <b>Name</b> attribute of the <a href="https://msdn.microsoft.com/45524773-3b61-44ac-a417-cfaac92af0a0">Identity</a> element in the package manifest.

The package name is not intended to be displayed to end users. Rather, the system uses it to uniquely identify the package.

The caller must free the memory allocated for <i>name</i> using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8665AC2B-4D06-4684-99B1-E22533CA04AA">IAppxManifestPackageId</a>
 

 

