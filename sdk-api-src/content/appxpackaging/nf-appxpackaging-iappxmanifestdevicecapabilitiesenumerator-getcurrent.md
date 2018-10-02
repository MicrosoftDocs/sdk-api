---
UID: NF:appxpackaging.IAppxManifestDeviceCapabilitiesEnumerator.GetCurrent
title: IAppxManifestDeviceCapabilitiesEnumerator::GetCurrent
author: windows-sdk-content
description: Gets the device capability at the current position of the enumerator.
old-location: appxpkg\iappxmanifestdevicecapabilitiesenumerator_getcurrent.htm
tech.root: appxpkg
ms.assetid: B9686070-645E-4F8A-8A1A-3DB80AEF4FF5
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxManifestDeviceCapabilitiesEnumerator interface, IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management],GetCurrent method, IAppxManifestDeviceCapabilitiesEnumerator.GetCurrent, IAppxManifestDeviceCapabilitiesEnumerator::GetCurrent, appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator::GetCurrent, appxpkg.iappxmanifestdevicecapabilitiesenumerator_getcurrent
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
 - IAppxManifestDeviceCapabilitiesEnumerator.GetCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestDeviceCapabilitiesEnumerator::GetCurrent


## -description


Gets the device capability at the current position of the enumerator.


## -parameters




### -param deviceCapability [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

The current device capability.


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



The caller must free the memory allocated for <i>deviceCapability</i> using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.

The enumerator returned can be empty. In this case, a call to  <a href="https://msdn.microsoft.com/52E0C961-F947-4F66-B3A0-21AB0F64C4B4">GetHasCurrent</a> returns <b>false</b>. If the enumerator is not empty, it points to the first element, and this method returns the first item. Subsequently, the user should use <a href="https://msdn.microsoft.com/2FD0F98C-2B20-47B2-8F86-F59E3E9B9086">MoveNext</a> to move through the items, and call <b>GetHasCurrent</b> before using <b>GetCurrent</b> to access the item.




## -see-also




<a href="https://msdn.microsoft.com/6A544E15-BB92-48C3-963D-789B04464277">IAppxManifestDeviceCapabilitiesEnumerator</a>
 

 

