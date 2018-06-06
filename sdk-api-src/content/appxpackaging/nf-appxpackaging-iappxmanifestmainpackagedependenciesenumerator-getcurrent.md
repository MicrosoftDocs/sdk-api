---
UID: NF:appxpackaging.IAppxManifestMainPackageDependenciesEnumerator.GetCurrent
title: IAppxManifestMainPackageDependenciesEnumerator::GetCurrent
author: windows-sdk-content
description: Gets the &lt;MainPackageDependency&gt; element at the current position of the enumerator.
old-location: appxpkg\iappxmanifestmainpackagedependenciesenumerator_getcurrent.htm
old-project: appxpkg
ms.assetid: 14C7F3F9-38FE-4FC2-9255-0A728A1488C0
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxManifestMainPackageDependenciesEnumerator interface, IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management],GetCurrent method, IAppxManifestMainPackageDependenciesEnumerator.GetCurrent, IAppxManifestMainPackageDependenciesEnumerator::GetCurrent, appxpackaging/IAppxManifestMainPackageDependenciesEnumerator::GetCurrent, appxpkg.iappxmanifestmainpackagedependenciesenumerator_getcurrent
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
 - IAppxManifestMainPackageDependenciesEnumerator.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestMainPackageDependenciesEnumerator::GetCurrent


## -description


Gets the &lt;MainPackageDependency&gt; element at the current position of the enumerator.


## -parameters




### -param mainPackageDependency [out, retval]

The current &lt;MainPackageDependency&gt; element.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The enumerator has passed the last item in the collection.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/EB511040-5011-4B79-AFEE-DFF42E11025B">IAppxManifestMainPackageDependenciesEnumerator</a>
 

 

