---
UID: NF:appxpackaging.IAppxPackageEditor.UpdatePackage
title: IAppxPackageEditor::UpdatePackage (appxpackaging.h)
author: windows-sdk-content
description: Updates an app package.
old-location: appxpkg\iappxpackageeditor_updatepackage.htm
tech.root: appxpkg
ms.assetid: 768D2997-A374-46FF-BA0D-14B266D3C83D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxPackageEditor interface [App packaging and management],UpdatePackage method, IAppxPackageEditor.UpdatePackage, IAppxPackageEditor::UpdatePackage, UpdatePackage, UpdatePackage method [App packaging and management], UpdatePackage method [App packaging and management],IAppxPackageEditor interface, appxpackaging/IAppxPackageEditor::UpdatePackage, appxpkg.iappxpackageeditor_updatepackage
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
 - IAppxPackageEditor.UpdatePackage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxPackageEditor::UpdatePackage


## -description


Updates an app package.


## -parameters




### -param baselinePackageStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of the baseline app package.


### -param deltaPackageStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of the delta (difference) app package.


### -param updateOption [in]

The update options.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/37D9494A-A5C0-4ABA-99BC-7F9B10E8D06C">IAppxPackageEditor</a>
 

 

