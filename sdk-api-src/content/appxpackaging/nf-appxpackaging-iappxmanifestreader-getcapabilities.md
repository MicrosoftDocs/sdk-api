---
UID: NF:appxpackaging.IAppxManifestReader.GetCapabilities
title: IAppxManifestReader::GetCapabilities
author: windows-sdk-content
description: Gets the list of capabilities requested by the package.
old-location: appxpkg\iappxmanifestreader_getcapabilities.htm
tech.root: appxpkg
ms.assetid: 5FCBD9E9-9A5E-49E1-8B80-8F84EDA8B07C
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetCapabilities, GetCapabilities method [App packaging and management], GetCapabilities method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetCapabilities method, IAppxManifestReader.GetCapabilities, IAppxManifestReader::GetCapabilities, appxpackaging/IAppxManifestReader::GetCapabilities, appxpkg.iappxmanifestreader_getcapabilities
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
 - IAppxManifestReader.GetCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestReader::GetCapabilities


## -description


Gets the list of capabilities requested by the package.


## -parameters




### -param capabilities [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4912BCB0-424B-40F9-BBD1-3AD0A60B3320">APPX_CAPABILITIES</a>*</b>

The list of capabilities requested by the package. This is a bitwise combination of  the values of the enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Capabilities are specified using the <a href="https://msdn.microsoft.com/ee6bf220-f139-4ad9-a7a7-e621c189b907">Capability</a> element in the package manifest.

If no package capabilities are defined in the manifest, this method returns <b>S_OK</b> with a zero value.




## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>
 

 

