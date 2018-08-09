---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfoEnumerator.GetCurrent
title: IAppxBundleManifestPackageInfoEnumerator::GetCurrent
author: windows-sdk-content
description: Gets the &lt;Package&gt; element at the current position of the enumerator.
old-location: appxpkg\iappxbundlemanifestpackageinfoenumerator_getcurrent.htm
old-project: appxpkg
ms.assetid: 52F525CB-162B-47E9-BF85-B920CBCCD983
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxBundleManifestPackageInfoEnumerator interface, IAppxBundleManifestPackageInfoEnumerator interface [App packaging and management],GetCurrent method, IAppxBundleManifestPackageInfoEnumerator.GetCurrent, IAppxBundleManifestPackageInfoEnumerator::GetCurrent, appxpackaging/IAppxBundleManifestPackageInfoEnumerator::GetCurrent, appxpkg.iappxbundlemanifestpackageinfoenumerator_getcurrent
ms.prod: windows
ms.technology: windows-sdk
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
 - IAppxBundleManifestPackageInfoEnumerator.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestPackageInfoEnumerator::GetCurrent


## -description


Gets the &lt;Package&gt; element at the current position of the enumerator.


## -parameters




### -param packageInfo [out, retval]

Type: <b><a href="https://msdn.microsoft.com/B9272875-E02A-4443-82B3-C64104E8291C">IAppxBundleManifestPackageInfo</a>**</b>

The current &lt;Package&gt; element. 


## -returns



Type: <b>HRESULT</b>

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
 




## -remarks



The enumerator’s position points to the first element by default. So, with a newly constructed enumerator that contains at least one element, <a href="https://msdn.microsoft.com/ED12F498-1F8D-45B2-9CFE-7215D2D87C3F">IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent</a> returns <b>TRUE</b> and <b>GetCurrent</b> returns the first element.




## -see-also




<a href="https://msdn.microsoft.com/4861D5CF-9FDC-4BAA-8462-D239DAEB5195">IAppxBundleManifestPackageInfoEnumerator</a>
 

 

