---
UID: NF:appxpackaging.IAppxManifestPackageId.GetVersion
title: IAppxManifestPackageId::GetVersion
author: windows-sdk-content
description: Gets the version of the package as defined in the manifest.
old-location: appxpkg\iappxmanifestpackageid_getversion.htm
old-project: appxpkg
ms.assetid: 85684359-9244-4130-BF0F-56DDB6427345
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetVersion, GetVersion method [App packaging and management], GetVersion method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetVersion method, IAppxManifestPackageId.GetVersion, IAppxManifestPackageId::GetVersion, appxpackaging/IAppxManifestPackageId::GetVersion, appxpkg.iappxmanifestpackageid_getversion
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxManifestPackageId.GetVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageId::GetVersion


## -description


Gets the version of the package as defined in the manifest.


## -parameters




### -param packageVersion [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a>*</b>

The version of the package.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -remarks



The version is specified using the <b>Version</b> attribute of the <a href="https://msdn.microsoft.com/45524773-3b61-44ac-a417-cfaac92af0a0">Identity</a> element in the package manifest. The specification in the manifest is in quad notation:

<i>major</i>.<i>minor</i>.<i>build</i>.<i>revision</i>

This method converts this notation to a <b>UINT64</b> value as follows:

<ul>
<li>The high-order word contains the major version</li>
<li>The next word contains the minor version</li>
<li>The next word contains the build number</li>
<li>The low-order word contains the revision</li>
</ul>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8665AC2B-4D06-4684-99B1-E22533CA04AA">IAppxManifestPackageId</a>
 

 

