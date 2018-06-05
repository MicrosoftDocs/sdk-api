---
UID: NN:appxpackaging.IAppxManifestProperties
title: IAppxManifestProperties
author: windows-sdk-content
description: Provides read-only access to the properties section of a package manifest.
old-location: appxpkg\iappxmanifestproperties.htm
old-project: appxpkg
ms.assetid: 5DA0A805-13D3-4977-8EFB-45E8B51AAF60
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxManifestProperties, IAppxManifestProperties interface [App packaging and management], IAppxManifestProperties interface [App packaging and management],described, appxpackaging/IAppxManifestProperties, appxpkg.iappxmanifestproperties
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
-	IAppxManifestProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestProperties interface


## -description


Provides read-only access to the properties section of a package manifest.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597607">GetBoolValue</a>
</td>
<td align="left" width="63%">
Gets the value of the specified Boolean element in the properties section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597621">GetStringValue</a>
</td>
<td align="left" width="63%">
Gets the value of the specified string element in the properties section.

</td>
</tr>
</table> 


## -remarks



The properties section of the manifest is defined using the <a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a> element.

This object can be retrieved using the <a href="https://msdn.microsoft.com/E507BA9D-D2CA-4B28-BD13-B820B666B4C6">IAppxManifestReader::GetProperties</a> method.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/E507BA9D-D2CA-4B28-BD13-B820B666B4C6">IAppxManifestReader::GetProperties</a>
 

 

