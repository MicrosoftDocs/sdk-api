---
UID: NN:appxpackaging.IAppxBundleManifestOptionalBundleInfoEnumerator
title: IAppxBundleManifestOptionalBundleInfoEnumerator
author: windows-sdk-content
description: Enumerates the optional bundle information from a bundle.
old-location: appxpkg\iappxbundlemanifestoptionalbundleinfoenumerator.htm
old-project: appxpkg
ms.assetid: 5BF38EC7-7C04-455B-AFAA-CC2A78E54A4F
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxBundleManifestOptionalBundleInfoEnumerator, IAppxBundleManifestOptionalBundleInfoEnumerator interface [App packaging and management], IAppxBundleManifestOptionalBundleInfoEnumerator interface [App packaging and management],described, appxpackaging/IAppxBundleManifestOptionalBundleInfoEnumerator, appxpkg.iappxbundlemanifestoptionalbundleinfoenumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBundleManifestOptionalBundleInfoEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestOptionalBundleInfoEnumerator interface


## -description


Enumerates the optional bundle information from a bundle.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleManifestOptionalBundleInfoEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleManifestOptionalBundleInfoEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleManifestOptionalBundleInfoEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C9C0E081-52AB-4B7F-B789-EC64B55EFA2A">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the optional bundle information at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C7473291-89EA-4412-848E-07257C0AC0FB">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is optional bundle information at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4A157CF1-8254-47FF-886A-77C15BDCDA76">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next set of optional bundle information.

</td>
</tr>
</table> 

