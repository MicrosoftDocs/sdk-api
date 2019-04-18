---
UID: NN:appxpackaging.IAppxManifestApplicationsEnumerator
title: IAppxManifestApplicationsEnumerator (appxpackaging.h)
author: windows-sdk-content
description: Enumerates the applications defined in the package manifest.
old-location: appxpkg\iappxmanifestapplicationsenumerator.htm
tech.root: appxpkg
ms.assetid: 49955DE0-A6BE-4FD7-B8E3-E4126B3C4B8F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxManifestApplicationsEnumerator, IAppxManifestApplicationsEnumerator interface [App packaging and management], IAppxManifestApplicationsEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestApplicationsEnumerator, appxpkg.iappxmanifestapplicationsenumerator
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
 - IAppxManifestApplicationsEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxManifestApplicationsEnumerator interface


## -description


Enumerates the applications defined in the package manifest.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestApplicationsEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestApplicationsEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestApplicationsEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54357408-57EA-4BD0-A619-F297C6248050">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the application at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3A497746-3AEB-4B20-9AD0-CD7B5F35853C">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is an application at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4F6EB510-4227-460B-9E2D-C304F33A931E">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next application.

</td>
</tr>
</table> 


## -remarks



Applications are specified using the <a href="https://msdn.microsoft.com/ad9e07fc-ba58-4465-b3fa-b330ba149f92">Applications</a> element in the package manifest.

This object can be retrieved using the <a href="https://msdn.microsoft.com/EC575692-93D6-43F1-857B-9A27DD50B8FC">IAppxManifestReader::GetApplications</a> method.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/16FC78D1-7387-4C90-9F63-BCFA110BC487">IAppxManifestApplication</a>



<a href="https://msdn.microsoft.com/EC575692-93D6-43F1-857B-9A27DD50B8FC">IAppxManifestReader::GetApplications</a>
 

 

