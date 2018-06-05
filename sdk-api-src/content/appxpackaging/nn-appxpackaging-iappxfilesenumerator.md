---
UID: NN:appxpackaging.IAppxFilesEnumerator
title: IAppxFilesEnumerator
author: windows-sdk-content
description: Enumerates the payload files in a package.
old-location: appxpkg\iappxfilesenumerator.htm
old-project: appxpkg
ms.assetid: A9BB3242-5CDA-49A9-8A7B-5A9A3E31B724
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxFilesEnumerator, IAppxFilesEnumerator interface [App packaging and management], IAppxFilesEnumerator interface [App packaging and management],described, appxpackaging/IAppxFilesEnumerator, appxpkg.iappxfilesenumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxFilesEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxFilesEnumerator interface


## -description


Enumerates the payload files in a package.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxFilesEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxFilesEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxFilesEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AFE7534D-862B-47C5-B6C0-633205E39FAB">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the payload file at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4CC798E4-5FD2-45DE-BD3A-0B036601BEDB">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a payload file at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EC27AB65-EC67-4F6B-A3B8-313FD0422FA2">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next payload file.

</td>
</tr>
</table> 


## -remarks



To get the footprint files, use the <a href="https://msdn.microsoft.com/8CCF9135-308F-4BDC-A67F-1E3ED2ACF565">IAppxPackageReader::GetFootprintFile</a> method.




## -see-also




<a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>
 

 

