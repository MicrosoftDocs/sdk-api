---
UID: NF:appxpackaging.IAppxBundleWriter3.Close
title: IAppxBundleWriter3::Close
author: windows-sdk-content
description: Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream.
old-location: appxpkg\iappxbundlewriter3_close.htm
old-project: appxpkg
ms.assetid: 7AD526CD-9FF2-4A2A-BD12-21A0A9E1BA6E
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: Close, Close method [App packaging and management], Close method [App packaging and management],IAppxBundleWriter3 interface, IAppxBundleWriter3 interface [App packaging and management],Close method, IAppxBundleWriter3.Close, IAppxBundleWriter3::Close, appxpackaging/IAppxBundleWriter3::Close, appxpkg.iappxbundlewriter3_close
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
 - IAppxBundleWriter3.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleWriter3::Close


## -description


Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream.


## -parameters




### -param hashMethodString [in]

The string value of the <b>HashMethod</b> attribute of the <a href="https://msdn.microsoft.com/75eed334-6c80-4eb3-8776-fc34d7aa5357">BlockMap</a> root element. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2596E2DA-D9B6-4BBE-AC05-5CE253CE6DDC">IAppxBundleWriter3</a>
 

 

