---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetFileName
title: IAppxBundleManifestPackageInfo::GetFileName method
author: windows-driver-content
description: Retrieves the file-name attribute of the package.
old-location: appxpkg\iappxbundlemanifestpackageinfo_getfilename.htm
old-project: appxpkg
ms.assetid: D8E827D4-0256-4598-A99A-EDB5FA14EDC2
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetFileName method [App packaging and management], GetFileName method [App packaging and management], IAppxBundleManifestPackageInfo interface, GetFileName,IAppxBundleManifestPackageInfo.GetFileName, IAppxBundleManifestPackageInfo, IAppxBundleManifestPackageInfo interface [App packaging and management], GetFileName method, IAppxBundleManifestPackageInfo::GetFileName, appxpackaging/IAppxBundleManifestPackageInfo::GetFileName, appxpkg.iappxbundlemanifestpackageinfo_getfilename
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBundleManifestPackageInfo.GetFileName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestPackageInfo::GetFileName method


## -description


Retrieves the file-name attribute of the package.


## -parameters




### -param fileName [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

A string that contains the file name of the package.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can pass the package file name that  <b>GetFileName</b> outputs to the <a href="https://msdn.microsoft.com/6ACAB26C-22FC-45D7-9F6A-98B56B615DCA">IAppxBundleReader::GetPayloadPackage</a> method to access the package’s contents.

When you're done using the file name, free the memory allocated for <i>fileName</i> by using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.




## -see-also




<a href="https://msdn.microsoft.com/B9272875-E02A-4443-82B3-C64104E8291C">IAppxBundleManifestPackageInfo</a>
 

 

