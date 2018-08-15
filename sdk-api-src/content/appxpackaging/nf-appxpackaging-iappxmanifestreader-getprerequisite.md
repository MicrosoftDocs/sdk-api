---
UID: NF:appxpackaging.IAppxManifestReader.GetPrerequisite
title: IAppxManifestReader::GetPrerequisite
author: windows-sdk-content
description: Gets the specified prerequisite as defined in the package manifest.
old-location: appxpkg\iappxmanifestreader_getprerequisite.htm
old-project: appxpkg
ms.assetid: 1CF44513-AA07-4591-9134-A156A538C8F1
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetPrerequisite, GetPrerequisite method [App packaging and management], GetPrerequisite method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetPrerequisite method, IAppxManifestReader.GetPrerequisite, IAppxManifestReader::GetPrerequisite, appxpackaging/IAppxManifestReader::GetPrerequisite, appxpkg.iappxmanifestreader_getprerequisite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
 - IAppxManifestReader.GetPrerequisite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestReader::GetPrerequisite


## -description


Gets the specified prerequisite as defined in the package manifest.


## -parameters




### -param name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The name of the prerequisite, either "OSMinVersion" or "OSMaxVersionTested".


### -param value [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a>*</b>

The specified prerequisite. In the manifest the dot-trio representation is Major.Minor.AppPlatform. This is converted to the 64-bit value as the follows:
The highest order word contains the Major version. The next word contains the Minor version.	The next word contains the optional AppPlatform version, if specified.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The prerequisite defined in <i>name</i> is not defined in the manifest.

</td>
</tr>
</table>
 




## -remarks



Prerequisites are specified using the <a href="https://msdn.microsoft.com/18c045dd-7e8c-431c-b3d8-bc3056575632">OSMinVersion</a> and <a href="https://msdn.microsoft.com/2f820978-5080-427d-b364-08951afae9ee">OSMaxVersionTested</a> elements in the package manifest.




## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>
 

 

