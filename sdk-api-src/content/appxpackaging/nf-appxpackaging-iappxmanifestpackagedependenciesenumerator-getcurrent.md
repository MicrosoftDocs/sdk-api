---
UID: NF:appxpackaging.IAppxManifestPackageDependenciesEnumerator.GetCurrent
title: IAppxManifestPackageDependenciesEnumerator::GetCurrent method
author: windows-driver-content
description: Gets the dependency package at the current position of the enumerator.
old-location: appxpkg\iappxmanifestpackagedependenciesenumerator_getcurrent.htm
old-project: appxpkg
ms.assetid: A7DDD037-2A0B-485A-AF1E-7A999780496B
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetCurrent method [App packaging and management], GetCurrent method [App packaging and management], IAppxManifestPackageDependenciesEnumerator interface, GetCurrent,IAppxManifestPackageDependenciesEnumerator.GetCurrent, IAppxManifestPackageDependenciesEnumerator, IAppxManifestPackageDependenciesEnumerator interface [App packaging and management], GetCurrent method, IAppxManifestPackageDependenciesEnumerator::GetCurrent, appxpackaging/IAppxManifestPackageDependenciesEnumerator::GetCurrent, appxpkg.iappxmanifestpackagedependenciesenumerator_getcurrent
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestPackageDependenciesEnumerator.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageDependenciesEnumerator::GetCurrent method


## -description


Gets the dependency package at the current position of the enumerator.


## -parameters




### -param dependency [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1A5515DA-4A9E-40EE-9AAC-F267DAE9DDBA">IAppxManifestPackageDependency</a>**</b>

The current dependency package.


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



The enumerator returned can be empty. In this case, a call to  <a href="https://msdn.microsoft.com/2D06DC83-B795-47F8-A05D-4DF4E86FEDFA">GetHasCurrent</a> returns <b>false</b>. If the enumerator is not empty, it points to the first element, and this method returns the first item. Subsequently, the user should use <a href="https://msdn.microsoft.com/DC30BC6F-C2E2-49B4-B0A8-1973880C9B4F">MoveNext</a> to move through the items, and call <b>GetHasCurrent</b> before using <b>GetCurrent</b> to access the item.




## -see-also




<a href="https://msdn.microsoft.com/A09709AE-301F-4457-8E02-1A88FB283A43">IAppxManifestPackageDependenciesEnumerator</a>
 

 

