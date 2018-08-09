---
UID: NF:appxpackaging.IAppxPackageEditor.UpdateEncryptedPackage
title: IAppxPackageEditor::UpdateEncryptedPackage
author: windows-sdk-content
description: Updates an encrypted app package.
old-location: appxpkg\iappxpackageeditor_updateencryptedpackage.htm
old-project: appxpkg
ms.assetid: 4D5E2F4B-00CE-4A0A-A514-3B66EC3065ED
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IAppxPackageEditor interface [App packaging and management],UpdateEncryptedPackage method, IAppxPackageEditor.UpdateEncryptedPackage, IAppxPackageEditor::UpdateEncryptedPackage, UpdateEncryptedPackage, UpdateEncryptedPackage method [App packaging and management], UpdateEncryptedPackage method [App packaging and management],IAppxPackageEditor interface, appxpackaging/IAppxPackageEditor::UpdateEncryptedPackage, appxpkg.iappxpackageeditor_updateencryptedpackage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
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
 - IAppxPackageEditor.UpdateEncryptedPackage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageEditor::UpdateEncryptedPackage


## -description


Updates an encrypted app package.


## -parameters




### -param baselineEncryptedPackageStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of the baseline encrypted app package.


### -param deltaPackageStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of the delta (difference) app package.


### -param updateOption [in]

The update options.


### -param settings [in]

The encrypted app package settings.


### -param keyInfo [in]

App package key information.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/37D9494A-A5C0-4ABA-99BC-7F9B10E8D06C">IAppxPackageEditor</a>
 

 

