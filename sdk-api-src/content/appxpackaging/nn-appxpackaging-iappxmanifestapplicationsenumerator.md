---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



Applications are specified using the <a href="https://msdn.microsoft.com/library/windows/hardware/jj159048">Applications</a> element in the package manifest.

This object can be retrieved using the <a href="https://msdn.microsoft.com/EC575692-93D6-43F1-857B-9A27DD50B8FC">IAppxManifestReader::GetApplications</a> method.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/16FC78D1-7387-4C90-9F63-BCFA110BC487">IAppxManifestApplication</a>



<a href="https://msdn.microsoft.com/EC575692-93D6-43F1-857B-9A27DD50B8FC">IAppxManifestReader::GetApplications</a>
 

 

