---
UID: NF:appxpackaging.IAppxManifestApplicationsEnumerator.GetCurrent
title: IAppxManifestApplicationsEnumerator::GetCurrent
author: windows-sdk-content
description: Gets the application at the current position of the enumerator.
old-location: appxpkg\iappxmanifestapplicationsenumerator_getcurrent.htm
tech.root: appxpkg
ms.assetid: 54357408-57EA-4BD0-A619-F297C6248050
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxManifestApplicationsEnumerator interface, IAppxManifestApplicationsEnumerator interface [App packaging and management],GetCurrent method, IAppxManifestApplicationsEnumerator.GetCurrent, IAppxManifestApplicationsEnumerator::GetCurrent, appxpackaging/IAppxManifestApplicationsEnumerator::GetCurrent, appxpkg.iappxmanifestapplicationsenumerator_getcurrent
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
 - IAppxManifestApplicationsEnumerator.GetCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- appxpackaging.h
: 
- IAppxManifestApplicationsEnumerator.GetCurrent
: 
---

# IAppxManifestApplicationsEnumerator::GetCurrent


## -description


Gets the application at the current position of the enumerator.


## -parameters




### -param application [out, retval]

Type: <b><a href="https://msdn.microsoft.com/16FC78D1-7387-4C90-9F63-BCFA110BC487">IAppxManifestApplication</a>**</b>

The current application.


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



The enumerator returned can be empty. In this case, a call to  <a href="https://msdn.microsoft.com/3A497746-3AEB-4B20-9AD0-CD7B5F35853C">GetHasCurrent</a> returns <b>false</b>. If the enumerator is not empty, it points to the first element, and this method returns the first item. Subsequently, the user should use <a href="https://msdn.microsoft.com/4F6EB510-4227-460B-9E2D-C304F33A931E">MoveNext</a> to move through the items, and call <b>GetHasCurrent</b> before using <b>GetCurrent</b> to access the item.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/49955DE0-A6BE-4FD7-B8E3-E4126B3C4B8F">IAppxManifestApplicationsEnumerator</a>
 

 

