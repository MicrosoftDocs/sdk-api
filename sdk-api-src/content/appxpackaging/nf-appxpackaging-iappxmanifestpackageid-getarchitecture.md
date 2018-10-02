---
UID: NF:appxpackaging.IAppxManifestPackageId.GetArchitecture
title: IAppxManifestPackageId::GetArchitecture
author: windows-sdk-content
description: Gets the processor architecture as defined in the manifest.
old-location: appxpkg\iappxmanifestpackageid_getarchitecture.htm
tech.root: appxpkg
ms.assetid: 0A332C96-9535-4BD3-B4D2-39559E430870
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetArchitecture, GetArchitecture method [App packaging and management], GetArchitecture method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetArchitecture method, IAppxManifestPackageId.GetArchitecture, IAppxManifestPackageId::GetArchitecture, appxpackaging/IAppxManifestPackageId::GetArchitecture, appxpkg.iappxmanifestpackageid_getarchitecture
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
 - IAppxManifestPackageId.GetArchitecture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestPackageId::GetArchitecture


## -description


Gets the processor architecture as defined in the manifest.


## -parameters




### -param architecture [out, retval]

Type: <b><a href="https://msdn.microsoft.com/8BC7ABF0-448F-4405-AA82-49C6DB3F230C">APPX_PACKAGE_ARCHITECTURE</a>*</b>

The architecture specified for the package.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Processor architecture information is specified using the <b>ProcessorArchitecture</b> attribute of the <a href="https://msdn.microsoft.com/45524773-3b61-44ac-a417-cfaac92af0a0">Identity</a> element in the package manifest.

If no architecture is defined in the manifest, this method returns the <b>APPX_PACKAGE_ARCHITECTURE_NEUTRAL</b> value of the  <a href="https://msdn.microsoft.com/8BC7ABF0-448F-4405-AA82-49C6DB3F230C">APPX_PACKAGE_ARCHITECTURE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/8665AC2B-4D06-4684-99B1-E22533CA04AA">IAppxManifestPackageId</a>
 

 

