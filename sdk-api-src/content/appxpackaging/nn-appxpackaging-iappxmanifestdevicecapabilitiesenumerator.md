---
UID: NN:appxpackaging.IAppxManifestDeviceCapabilitiesEnumerator
title: IAppxManifestDeviceCapabilitiesEnumerator
author: windows-sdk-content
description: Enumerates the device capabilities defined in the package manifest.
old-location: appxpkg\iappxmanifestdevicecapabilitiesenumerator.htm
old-project: appxpkg
ms.assetid: 6A544E15-BB92-48C3-963D-789B04464277
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxManifestDeviceCapabilitiesEnumerator, IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management], IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator, appxpkg.iappxmanifestdevicecapabilitiesenumerator
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
-	IAppxManifestDeviceCapabilitiesEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestDeviceCapabilitiesEnumerator interface


## -description


Enumerates the device  capabilities defined in the package manifest. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestDeviceCapabilitiesEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestDeviceCapabilitiesEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestDeviceCapabilitiesEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B9686070-645E-4F8A-8A1A-3DB80AEF4FF5">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the device capability at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52E0C961-F947-4F66-B3A0-21AB0F64C4B4">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a device capability at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2FD0F98C-2B20-47B2-8F86-F59E3E9B9086">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next device capability.

</td>
</tr>
</table> 


## -remarks



Device capabilities are specified using the <a href="https://msdn.microsoft.com/4353c4fd-f038-4986-81ed-d2ec0c6235ef">DeviceCapability</a> element in the package manifest.

This object can be retrieved using the <a href="https://msdn.microsoft.com/06257DB1-992E-4A8D-8221-76DA3DF0FA1F">IAppxManifestReader::GetDeviceCapabilities</a> method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LPWSTR deviceCapability = NULL;
bool hasCurrent = false;
	
for (deviceCapabilitiesEnumerator-&gt;GetHasCurrent(&amp;hasCurrent); hasCurrent == true;
	deviceCapabilitiesEnumerator-&gt;MoveNext(&amp;hasCurrent))
{
	hr = deviceCapabilitiesEnumerator-&gt;GetCurrent(&amp;deviceCapability); 

	...

	if (deviceCapability)
	{
		CoTaskMemFree(deviceCapability);
	}
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/06257DB1-992E-4A8D-8221-76DA3DF0FA1F">IAppxManifestReader::GetDeviceCapabilities</a>
 

 

