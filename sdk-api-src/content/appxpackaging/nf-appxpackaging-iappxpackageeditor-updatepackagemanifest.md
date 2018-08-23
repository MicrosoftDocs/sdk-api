---
UID: NF:appxpackaging.IAppxPackageEditor.UpdatePackageManifest
title: IAppxPackageEditor::UpdatePackageManifest
author: windows-sdk-content
description: Updates an app package manifest.
old-location: appxpkg\iappxpackageeditor_updatepackagemanifest.htm
old-project: appxpkg
ms.assetid: A30B3A7E-28FA-4780-9ED3-4F19887189E8
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: IAppxPackageEditor interface [App packaging and management],UpdatePackageManifest method, IAppxPackageEditor.UpdatePackageManifest, IAppxPackageEditor::UpdatePackageManifest, UpdatePackageManifest, UpdatePackageManifest method [App packaging and management], UpdatePackageManifest method [App packaging and management],IAppxPackageEditor interface, appxpackaging/IAppxPackageEditor::UpdatePackageManifest, appxpkg.iappxpackageeditor_updatepackagemanifest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IAppxPackageEditor.UpdatePackageManifest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageEditor::UpdatePackageManifest


## -description


Updates an app package manifest.


## -parameters




### -param packageStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of the app package associated with the manifest to be updated.


### -param updatedManifestStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of the updated app package manifest.


### -param isPackageEncrypted [in]

Flag to specify whether the package is encrypted.


### -param options [in]

Options for app package manifest validation.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/37D9494A-A5C0-4ABA-99BC-7F9B10E8D06C">IAppxPackageEditor</a>
 

 

