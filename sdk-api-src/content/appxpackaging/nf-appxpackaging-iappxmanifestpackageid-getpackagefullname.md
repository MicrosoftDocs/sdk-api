---
UID: NF:appxpackaging.IAppxManifestPackageId.GetPackageFullName
title: IAppxManifestPackageId::GetPackageFullName
author: windows-sdk-content
description: Gets the package full name.
old-location: appxpkg\iappxmanifestpackageid_getpackagefullname.htm
old-project: appxpkg
ms.assetid: 514D2E04-5CA5-4F45-A6D8-96866588EECF
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetPackageFullName, GetPackageFullName method [App packaging and management], GetPackageFullName method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetPackageFullName method, IAppxManifestPackageId.GetPackageFullName, IAppxManifestPackageId::GetPackageFullName, appxpackaging/IAppxManifestPackageId::GetPackageFullName, appxpkg.iappxmanifestpackageid_getpackagefullname
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestPackageId.GetPackageFullName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageId::GetPackageFullName


## -description


Gets the package full name.


## -parameters




### -param packageFullName [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

The package full name.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -remarks



The package full name string is a case-insensitive string, which can be used to uniquely identify the package. 

This string  is a serialized form of the package ID, and it is suitable for naming objects such as files and directories.

The caller must free the memory allocated for <i>packageFullName</i> using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8665AC2B-4D06-4684-99B1-E22533CA04AA">IAppxManifestPackageId</a>
 

 

